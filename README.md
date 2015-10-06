C# Resque Worker Example
============

This repository uses [Alex Demers - CSharp-Resque](https://github.com/alexdemers/csharp-resque) library which can be installed through the Nuget Package Manager. **This is not a production ready project, it is simply an example of how to use CSharp-Resque to process a Resque flavored queue.**

Looking for a cloud hosted Redis solution? Try [Redis Cloud](https://redislabs.com/redis-cloud)

## Troubleshooting
#### Processing jobs from another Resque language library
CSharp-Resque uses an id in the job to monitor the status of the job. Not all libraries do this such as [Node-Resque](https://github.com/taskrabbit/node-resque). This will throw an exception in the library. This [fork](https://github.com/atorres757/csharp-resque) contains a work around for this issue but it will require you to clone and build the project and you will have to update your references from this fork.

#### Versioning issues with Nuget package
When installing CSharp-Resque via Nuget some of the dependencies are installed with different versions than what was used to compile CSharp-Resque. This issue should be resolved in this repository but if not try updating the dependencies to the versions in the packages.config file.
Open the Package Manager Console and type the following:
```
Install-Package ServiceStack.Common -Version 3.9.49
Install-Package ServiceStack.Text -Version 3.9.49
```
