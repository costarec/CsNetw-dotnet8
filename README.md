# CsNetw-dotnet8
Port of Sean Burns Hands-on Network Programming with C# and .NET Core to use .NET 8.0

This is a modification of the source code distribution package provided by author Sean Burns in his book, 
"Hands-On Network Programming with C# and .NET Core" published 2019 by Packt> Publishing.

This distribution has been cleaned up and reorganized so that it can be easily opened in Visual Studio
as a single .SLN solution file, with all .csproj files loading correctly in the solution explorer window.

I did this only to faciliate using the software as examples in my courses:
TINFO-200 Programming II for ITS at the University of Washington Tacoma

I modified the configuration of the .csproj file projects to indicate a target of .NET 8.0 in place of dotnet2.2
Some additional source code was modified to avoid deprecated nuget dependencies and changes in the corresponding code.
Most of these modifications had to do with the use of the fluent API in Program.cs for enabling MVC and updating some deprecated network nuget package dependencies.

None of the basic source code logic or networking logic of the original source code was altered.

My intention was simply to provide students with an easy quick way to load all the programs into the Visual Studio 2022 IDE so they would be more likely to engage in experimenting and learning from the sample programs without having to focus on path, build, and configuration inconsistencies from example to example. 

You should be able to download the repos as a zip, unzip it on your drive, double click the top level .SLN file to open in Visual Studio and do a Build->Batch Build of the entire solution. 

There are still some compile warnings from a Rebuild All result but they are acceptable for my use. If they are not acceptable to you, please fix them as you see fit. This entire book's examples should be fully compatible with .NET 8.

An alternative to build all is to: open the Tools->Command Line->Developer PowerShell and issue the cmd:

msbuild -t:rebuild -p:configuration=debug  (or release)

Previous command builds the 50 CS projects.

--chuck costarella, 2024-04-27
