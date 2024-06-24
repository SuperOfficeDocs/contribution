---
uid: crmscript-yaml-reference
language: en
title: YAML API reference
description: How to work with CRMScript API reference on SuperOfficeDocs
topic: concept
keywords: YamlMime:ManagedReference, YAML, ManagedReference, CRMScript
date: 12.01.2021
author: Bergfrid Dias
---

<!-- markdownlint-disable-file MD013-->

# YAML format API reference

Unlike the other SuperOffice API references, the CRMScript reference documentation is maintained manually and not generated from source code. This will change, but for now, you need to understand how these files are formatted, structured, and connected should you need to add or update something.

We use **YAML ManagedReference files**. In short, these represent a structured data model in YAML and follow the [Metadata Format for .NET Languages][2].

> [!NOTE]
> YAML is **very picky** when it comes to whitespace and indentation.

## Terminology

The specification lists three types of items: namespaces, types, and members. The CRMScript language doesn't have namespaces, but we have used namespace items to group the information. Thus the mapping looks like this:

| ManagedReference item | CRMScript equivalent | Example UID |
|---|---|---|
| Namespace | Group of classes | CRMScript.Global |
| Type | A class or enum | CRMScript.Global.String |
| Member | A method or enum value | CRMScript.Global.String.append(String) |

**Available namespaces:**

* CRMScript.Global = Basic data types
* CRMScript.Native = Classes native to CRMScript
* CRMScript.NetServer = Classes from the NetServer APIs made available through CRMScript
* CRMScript.Event = Trigger scripts

## UIDs

Each CRMScript class, method, and enum has a unique ID. The UID is used for:

* The filename - \<UID>.yml
* The item definition
* Connecting an item to a parent (for example, a method to a class)
* Creating automatic links to a parameter or return type
* Creating explicit cross-references to another item (both YAML to YAML and Markdown to YAML)

## File format

* The first line of each file is `### YamlMime:ManagedReference`. (Magic string, info to DocFX about the format.)
* Then follows an array of items, starting with the line `items:`
* Last, you'll find an array of references starting with the line `references:`

In both arrays, lines starting with `- uid:` mark the beginning of an entry.

The contents of the item array depend on whether it is a class or namespace.

## Properties

### Names

Different displays require different granularity of information. Thus we have multiple name-related properties:

```yml
name: toUpper()
nameWithType: String.toUpper()
fullName: CRMScript.Global.String.toUpper()
```

### Langs

<!-- markdownlint-disable-next-line MD044 -->
Should always be 'crmscript'.

```yml
langs:
  - crmscript
```

### Type

* Namespace
* Class
* Constructor
* Method
* Enum
* Field

```yml
type: Method
```

### Children

List of UIDs, one per line, in the order of appearance.

```yaml
children:
  - CRMScript.Global.Bool.#ctor
  - CRMScript.Global.Bool.#ctor(Bool)
  - CRMScript.Global.Bool.toInteger()
  - CRMScript.Global.Bool.toString()
```

* For a namespace, this is the list of classes and enums belonging to that group.
* For a class, these are the constructors and methods.
* For an enum, this is the available fields (values).

### Summary

A one-line description of what the class or method does. Use an active verb.

```yml
summary: "\nConverts a boolean value to its integer representation (0 or 1).\n"
```

* It must be enclosed in double quotation marks and start and end with a newline `\n`.
* Quotation marks inside the string must be written as `&quot;`.
* Line breaks are created with `<p></p>\n`.

### Remarks

Additional information such as exceptions, available options, warnings. For methods and constructors only.

```yml
remarks: "\nIf any white-space characters are present in the string, the method will return false!\n"
```

Same formatting rules as for the summary.

### Example

A textual example, CRMScript code, or both.

```yml
example:
  - "\nPrints the length of a string: <pre><code>String txt = &quot;Wergelandsveien&quot;;\nprintLine(txt.getLength().toString());</code></pre>Outputs 15.\n"
```

* It must be enclosed in double quotation marks and start and end with a newline `\n`.
* Quotation marks inside the string must be written as `&quot;`. Even inside `<code>` tags!
* Code must be wrapped inside `<pre><code></code></pre>`.
* Line breaks and indentation in code are created with `\n` and `\t` respectively. To output these characters, escape with a slash.

> [!NOTE]
> Although the specification supports multiple examples, the interactive features of our site do not. Keep it to one element.

### Syntax

**Method without parameters:**

```yml
syntax:
  content: Integer getLength()
  parameters: []
  return:
    type: CRMScript.Global.Integer
    description: "The number of characters in the String."
```

**Method with parameters:**

```yml
syntax:
  content: String wrap(Integer length, Bool ignoreQuote)
  parameters:
  - id: length
    type: CRMScript.Global.Integer
    description: "The number of characters per line after wrapping."
  - id: ignoreQuote
    type: CRMScript.Global.Bool
    description: "True if you do not want quoted lines to be wrapped, else false."
  return:
    type: CRMScript.Global.String
```

**Method without return type:**

```yml
syntax:
  content: Void SetValue(String colName, String value)
  parameters:
  - id: colName
    type: CRMScript.Global.String
    description: "Column name."
  - id: value
    type: CRMScript.Global.String
    description: "Value that should be stored."
  return:
    type: CRMScript.Global.Void
```

> [!NOTE]
> Every UID listed as a type in the syntax must also be listed in the references at the end of the file.
>
> If the type is an array, you need to define it with as spec.

```yml
- uid: CRMScript.Global.String
  commentId: T:CRMScript.Global.String
  isExternal: true
  name: String
  nameWithType: String
  fullName: CRMScript.Global.String
- uid: CRMScript.Global.String[]
  isExternal: true
  name: String[]
  nameWithType: String[]
  fullName: CRMScript.Global.String[]
  spec.crmscript:
  - uid: CRMScript.Global.String
    name: String
    nameWithType: String
    fullName: CRMScript.Global.String
    isExternal: true
  - name: '[]'
    nameWithType: '[]'
    fullName: '[]'
```

### SuperOffice-specific properties

* `so.version`: when was the item added or updated
* `so.intellisense`: string used when building the in-application CRMScript intellisense

## Common tasks

<!-- markdownlint-disable-next-line MD044 -->
If you have suggestions or want to request changes, you can [create a site feedback issue][1]. We also welcome pull requests to the crmscript repo.

> [!TIP]
> To find the appropriate YAML file, look at the URL and substitute *.html* with *.yml*.
>
> For example, the CRMScript.Global.String.html page comes from the *CRMScript.Global.String.yml* file.

### Fix typo, add or update text

1. Open the file and search for the typo.
2. Change the `summary`, `remarks`, `examples`, or `description` property.

### Change return type

1. Open the file and go to the method. (Search for the UID.)
2. Update both the first word of the `syntax.content` property and the `syntax.return.type` property.
3. Remember to update the references if you bring in a new type.

```yml
syntax:
  content: String xmlEncode()
  parameters: []
  return:
    type: CRMScript.Global.String
```

### Fix broken link

Broken links are usually caused by misspelled or incomplete UIDs.

Links **from a CRMScript YAML** file to another should be formatted with an HTML xref element.

```yml
<xref href=\"UID\" data-throw-if-not-resolved=\"false\"></xref>
```

If the UID is CRMScript.NetServer.TicketSecurityLevel, the correct link is:

```yml
<xref href=\"CRMScript.NetServer.TicketSecurityLevel\" data-throw-if-not-resolved=\"false\"></xref>
```

The quotes surrounding attribute values must be escaped. The entire element must be inside single or double quotes.

Links **from Markdown to YAML** reference should be formatted as `<xref:UID>`. Don't add any spaces!

```markdown
<xref:CRMScript.Native.EventData.getType()>
```

### Add a method

1. Locate and open the class file.
2. Add a `-uid:` entry to the items array. Remember to update the references if you bring in a new type.
3. Add a line with the new UID to the list of children. Sort alphabetically and place constructors at the top.
4. Set the value of `so.version` to when it will be available. If you don't know, comment on the issue/PR so we can follow up.

### Add a class

1. Decide the UID for the new class and create the YAML file.
2. Populate the file
3. Add a line with the new UID to the list of children in the appropriate namespace file. Sort alphabetical
4. Add the new class to the references in the namespace file.
5. Add the new file to the TOC (*toc.yml*). Sort alphabetically.

<!-- Referenced links -->
[1]: https://github.com/SuperOfficeDocs/feedback/issues/new?assignees=&labels=&template=improve-the-site.md&title=
[2]: https://dotnet.github.io/docfx/spec/metadata_dotnet_spec.html

<!-- Referenced images -->
