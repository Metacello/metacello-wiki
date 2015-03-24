To install the latest version of Metacello (as of version [1.0-beta.28](http://code.google.com/p/metacello/wiki/10betaVersionDescriptions#1.0-beta.28)):

## Pharo ##
Execute the following expression in a workspace:
```
Gofer new
  squeaksource: 'MetacelloRepository';
  package: 'ConfigurationOfMetacello';
  load.
(Smalltalk at: #ConfigurationOfMetacello) perform: #load.
```
## Squeak ##
Execute the following expression in a workspace:
```
Installer squeaksource
    project: 'MetacelloRepository';
    install: 'ConfigurationOfMetacello'. 
(Smalltalk at: #ConfigurationOfMetacello) perform: #load.
```
Note that #loadLatestVersion loads a minimum install of Metacello.
## OB Tools ##
To load the OB-based tools, execute the following expression in a workspace (after [loading Metacello](DownloadMetacello#Pharo.md) into your image):
```
     (ConfigurationOfMetacello project version: #stable) load: #('UI').
```

## Tutorial & API Reference ##
To load the [tutorial](Tutorial.md) and [API reference](APIReference.md), execute the following expression in a workspace (after [loading Metacello](DownloadMetacello#Pharo.md) into your image):
```
     ConfigurationOfMetacello project latestVersion load: #('Tutorial').
```
## Create Your Own Metacello Configuration ##
To create your own Metacello configuration, run the ProfStef tutorial:
```
ConfigurationOfMetacello project latestVersion load: #('Tutorial').
ProfStef goOn: MetacelloDevelopmentProcess.
```

If you don't have access to ProfStef, follow [these steps](CreateMetacelloConfiguration.md).