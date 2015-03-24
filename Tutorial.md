## Image-based Tutorial ##
To run the Tutorial, first [load](DownloadMetacello#Tutorial_&_API_Reference.md) the Metacello Tutorial into your image:
```
(ConfigurationOfMetacello project version: #stable) load: #('Tutorial').
```

Then using ProfStef:
```
ProfStef goOn: MetacelloConfigurationTutorialPart1.
ProfStef goOn: MetacelloConfigurationTutorialPart2.
ProfStef goOn: MetacelloDevelopmentProcess.
```
Or via browser:
  1. Open two code browsers on the MetacelloTutorialConfig class.
  1. In the lefthand browser view the methods in the 'lessons' category.
  1. In the righthand browser view the '--all--' category.
  1. Read the comments in lesson01 through lesson13, then read lesson07 through lesson14 in the MetacelloProjectRefTutorialConfig class for a tutorial covering project references.

After taking the tutorial, visit [API reference page](APIReference.md) for an overview of the full configuration API.

To create your own Metacello configuration, run the ProfStef tutorial:
```
ConfigurationOfMetacello project latestVersion load: #('Tutorial').
ProfStef goOn: MetacelloDevelopmentProcess.
```

If you don't have access to ProfStef, follow [these steps](CreateMetacelloConfiguration.md).