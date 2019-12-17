# Generating nuget

- Download `nuget` or install package `Install-Package Nuget.CommandLine`.
- Create `nuspec` file.
    - If using nuget package, create `nuspec` using `nuget spec`.    
    - (or) manually create the spec file.
```
<?xml version="1.0" encoding="utf-8"?>
<package xmlns="http://schemas.microsoft.com/packaging/2010/07/nuspec.xsd">
  <metadata>
    <id>PackageId</id>
    <version>PackageVersion-alpha</version>
    <authors>Author</authors>
    <owners>Owner</owners>
    <requireLicenseAcceptance>false</requireLicenseAcceptance>
    <description>Description</description>
    <dependencies />
  </metadata>
</package>
```
- If version has `-<any string>`, nuget considers that as `pre-release` version.
- Create package using `nuget pack`.
- Create a folder to acc as package source. Add it to list of package sources in Visual Studio
- Add package to source using `nuget add .\<package>.nupkg -source <package folder path>`
- While adding nugets, if it is pre-release, make sure to check the pre-release checkbox.
