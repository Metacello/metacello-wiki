As of version [1.0-beta.25](http://code.google.com/p/metacello/wiki/10betaVersionDescriptions#1.0-beta.25)

# Commands #

![http://gemstonesoup.files.wordpress.com/2010/03/metacellotools.png](http://gemstonesoup.files.wordpress.com/2010/03/metacellotools.png)

  * [Save Packages (nested)](MetacelloTools#Save_Packages_(nested).md)
  * [Spawn New Version](MetacelloTools#Spawn_New_Version.md)
  * [Update Package Methods](MetacelloTools#Update_Package_Methods.md)
  * [Current Project Version](MetacelloTools#Current_Project_Version.md)
  * [Load Latest Packages](MetacelloTools#Load_Latest_Packages.md)
  * [Load Project Version](MetacelloTools#Load_Project_Version.md)
  * [Save Project](MetacelloTools#Save_Project.md)
  * [Update Project](MetacelloTools#Update_Project.md)

## Save Packages (nested) ##
Traverses all of the projects that are dependents of the selected project. For each project a list of dirty packages associated with that projects is created and you are prompted for a commit comment that is used as the commit for each of the mcz files.

You are then prompted to [Update Package Metods](MetacelloTools#Update_Package_Methods.md) and then given an opportunity to commit the configuration mcz file.

After all projects with dirty methods have been saved, a final pass is made to check for dirty project configurations. You are prompted to commit each of them.
## Spawn New Version ##
Generates a new version method prompting for source version, version number and the new methods selector. The package specs for the new method reflect the currently loaded Monticello package versions, like the [Update Package Methods](MetacelloTools#Update_Package_Methods.md) command.
## Update Package Methods ##
Automatically updates the package spec metadata for the selected version (i.e., modifies and compiles the methods with the #packages:attribute: pragma for the appropriate version to match the currently loaded Monticello package versions). After the methods are update you are prompted to [Save Project](MetacelloTools#Save_Project.md).
## Current Project Version ##
Displays the current version of the selected Metacello project. The version is calculated by comparing the currently loaded Monticello packages to those specified in the version spec. A leading ‘~’ means that the version is partially loaded (i.e., not all of the packages associated with the project have been loaded into the image).
## Load Latest Packages ##
Prompts for the #baseline version of the selected Metacello project to be loaded, then loads the latest version of each of the named packages.
## Load Project Version ##
Prompts for the version of the selected Metacello project to be loaded, then loads all of the packages in the project. By default the 'default' group is loaded. however, if so enabled, the last set of packages that were loaded will be loaded for in new version. To enable the recording of load information, see **#lastMetacelloVersionLoad** and **#metacelloVersion:loads:** in the class **MetacelloConfigTemplate**.
## Save Project ##
Saves the selected Metacello project to the repository specified by the project package of the selected version. You are prompted for version name and commit comment.
## Update Project ##
Loads the latest Monticello package version from the repository specified in the project package of the selected version of the Metacello project. Remember that you are simply loading the Metacello project metadata, so it doesn’t hurt to have the latest metadata loaded. Once the latest version is loaded, you are prompted to [Load Project Version](MetacelloTools#Load_Project_Version.md).