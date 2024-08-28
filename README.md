---
description: Welcome to Metalinker!
icon: hand-wave
---

# Welcome

Welcome to Metalinker! It's a C# library that allows you to parse any and all of the Metalink files that are built using Metalink 3.0 or 4.0 compliant generators. This is useful to give your download managers a boost. To use this library, go to any page in the left side of the screen.

## Installation

This library is very easy to install. It's available at [NuGet](https://www.nuget.org/packages/SpecProbe/). Just follow these steps:

1. Open your project file (`.csproj` or `.fsproj`)
2. Place the `PackageReference` line on a property group like so:
   * `<PackageReference Include="Metalinker" Version="x.x.x" />`
   * ...where `Version` is the current version of the library
3. Run a package restore using `dotnet restore`

If you follow these steps correctly, you should be able to use this library's functions.
