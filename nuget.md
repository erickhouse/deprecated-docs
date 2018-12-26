
# Nuget

## Key Terms

| Term | Description      |
| ---- | ---------------- |
| nuget.config     | A file that configures nuget on a specific project |
| packages.config     | only used with the package reference format in .csproj files |
|NUGET_PACKAGES| An environment variable that can override the current nuget config|
|.nupkg| The binary file that is created after `dotnet pack` is run. This binary does not contain dependencies|
|.nuspec|Generated with the `dotnet pack` cmd. Describes the .nupkg|
|apiKey| The key required to push to a remote nuget repository (acquired through a nuget account)|
|~\\.nuget\packages|Default location where nuget packages are stored|

## Resources

### Configure nuget reference

https://docs.microsoft.com/en-us/nuget/reference/nuget-config-file

### Nuget cli reference

https://docs.microsoft.com/en-us/nuget/tools/nuget-exe-cli-reference

Note:

- The cli `nuget` and `dotnet nuget` don't seem to be the same thing even though they have very similar behaviors.

## Nuget Sources

A source is simply a place where nuget packages are located. It can be a local folder, a server, nuget.org, etc...

sources can be configured using the cli or the `nuget.config` file. If using the `nuget.config` file, visual studio will read in the sources and display them in the `Manage nuget packages` GUI.

```xml

<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <clear />
    <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
    <add key="nuget.physio-labs.com" value="https://nuget.physio-labs.com/api/v2" />
    <add key="local" value="%userprofile%\.nuget\packages" />
  </packageSources>
</configuration>

```

Once a source has been configured you can use its alias with other nuget operations

`dotnet nuget ... --source local`

## .nuspec

Is mostly controlled by the build process. It gets data from the .csproj such as 

```xml
<PackageId>project_name</PackageId>
<Version>1.0.0</Version>
<Authors>your_name</Authors>
<Company>your_company</Company>
```

## Publish

`dotnet nuget push {project}.nupkg -k {apiKey} -s {the nuget source}`

## Versioning

Nuget uses semver