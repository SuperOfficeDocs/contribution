---
uid: get-superoffice-docs-running-locally
locale: en
title: Get SuperOfficeDocs running locally
description: Get SuperOfficeDocs running locally
so.topic: howto
so.date: 04.19.2021
so.author: Tony Yates
---

# Get SuperOfficeDocs running locally

The project uses the [DocFX][1] library to pull XML comments from the SuperOffice Platform source code and combine that with articles written in Markdown to form the documentation for SuperOffice.

## Installing Git

If you do not have Git installed, you will need to install Git first. You can find instructions on installing Git from [here][2].

## Installing DocFX

DocFX may be installed on Windows via **Chocolatey** by calling `choco install docfx -y`

If you are on MacOS, you can install it with **Homebrew** `brew install docfx`

Or you can download and unzip *docfx.zip* from [GitHub][3], extract it to a folder, and then set your `PATH` to that folder so you can run it anywhere.

## Setting up the SuperOfficeDocs project

After installing DocFX, the next step is to clone this repo. This will simply create a copy of the repo (files and folders) on your local machine so that you can work with them.

Note the following example command clones the repo to *c:\dev* or the location of choice on your machine.

```bash
c:\dev> git clone https://github.com/SuperOfficeDocs/superoffice-docs.git
```

The previous command will have created a folder called *superoffice-docs* in the *c:\dev* folder. Navigate to that directory by using the **cd** (Change Directory) command. `cd` into the `superoffice-docs` folder.

```bash
c:\dev> cd superoffice-docs
```

> [!NOTE]
> Relative links between SuperOfficeDocs repositories use the repository name! We recommend that you clone all relevant repositories from SuperOfficeDocs to the **same folder** (such as *c:\dev*) and **don't change the name**.

### Include API documentation

If you want to include the API documentation, you'll need to download the [SuperOffice NuGet packages][4] into a **sub-folder** of the *superoffice-docs* root folder called *src*. The reason is that the project reads the XML comments in the source code and creates API documentation from that, in addition to the documentation center articles.

From the tools folder, run the `nuget install` command to unpack the contents of the package into an output directory, then copy the DLLs and XML documentation files into a folder with the same name as the package to the src folder.

```dotnetcli
./tools/nuget install SuperOffice.WebApi -Version 1.0.0-preview3 -Source $pwd -OutputDirectory packages
copy D:\superoffice-docs\build-docs\packages\SuperOffice.WebApi.1.0.0-preview3\lib\netstandard2.0\*.* src\SuperOffice.WebApi\
```

> [!NOTE]
> Don't worry about the SuperOffice source code existing here. The documentation is generated from the XML documentation file.

## Running the SuperOffice docs project locally

You should now be able to run the development version of the docs locally with the following command:

```bash
docfx --serve
```

> [!NOTE]
> You should run your shell in administrator mode for this to work!

The first time, the compilation process could take quite a while. You may see a couple of warning messages. Eventually, you should see a message similar to:

```bash
Serving "C:\dev\superoffice-docs\_site" on https://localhost:8080
```

Open that page up in your browser to see the documentation.

[https://localhost:8080](https://localhost:8080)

> [!NOTE]
> Depending on the configuration of your development environment, you may need to use the non-SSL version of the local website URL instead.

[http://localhost:8080](http://localhost:8080)

<!-- Referenced links-->
[1]: https://dotnet.github.io/docfx/
[2]: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[3]: https://github.com/dotnet/docfx/releases
[4]: https://www.nuget.org/profiles/SuperOffice
