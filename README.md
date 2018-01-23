# Example for global .NET Core tools

This repository contains example tool projects that show how global tools can be used.
This sample needs a .NET Core Sdk version of at least 2.1.300 - Preview.

## How to run

Clone the repository, and execute this at its root directory:

```sh
$ dotnet pack -c Release
$ dotnet install tool -g sayhi.tool
$ dotnet install tool -g greet.tool
```

You may see warnings about prerelease version numbers, which you can ignore if you are using preview tooling.

Then open a new command line window / terminal (you can skip this if your environment is already set up) and run the commands:

```
$ sayhi
sayhi
Hi martin!
```

The second command is named `dotnet-greet` which means that you can also run this as:

```
> dotnet greet
Hi martin.ullrich!
```

Note that at the time of publishing (january 2018), there is a bug which prohibits this from being run as a CLI verb. You can run it using `dotnet-greet` (with a hyphen instead of a space) instead.