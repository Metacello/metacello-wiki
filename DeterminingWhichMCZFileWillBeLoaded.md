Here is an example where I’ve printed out the result of doing a fetch on the latest version of Pier from a Pharo Dev image and you can seewhich mcz files will be loaded into the image:
```
ConfigurationOfPier project latestVersion fetch loadDirective.
```
```
linear load :
  explicit load : 1.2.1.3 [ConfigurationOfPier]
  explicit load : 1.2.1.3 [ConfigurationOfPier]
  linear load : 1.2.1.3 [ConfigurationOfPier]
    linear load : 1.2.1.4 [ConfigurationOfMagritte]
      load : Magritte-Model-lr.367
    explicit load : 1.2.1.4 [ConfigurationOfMagritte]
    linear load : 1.2.1.4 [ConfigurationOfMagritte]
      explicit load : 2.8.4.2 [ConfigurationOfSeaside28]
      linear load : 2.8.4.2 [ConfigurationOfSeaside28]
        linear load : 1.0 [ConfigurationOfKomHttpServer]
          load : DynamicBindings-lr.11
          load : KomServices-gc.19
          load : KomHttpServer-lr.51
        load : Seaside2.8a1-pmm.596
        load : RSRSS2-pmm.12
        load : Scriptaculous-lr.250
        load : Comet-lr.29
      load : Magritte-Seaside-lr.316
      load : Magritte-Tests-lr.159
    load : Pier-Model-lr.351
    load : Pier-Tests-lr.150
    load : Pier-Seaside-lr.451
    load : Pier-Security-lr.144
    load : Pier-Blog-lr.134
    load : Pier-Squeak-Persistency-kph.24
```
Of course, this kind of report is a lot more useful if you’ve already got Pier loaded and want to know what will be loaded if you do an upgrade. Here’s the report when run in an image into which Pier 1.2.1 has already been loaded:
```
ConfigurationOfPier project latestVersion fetch loadDirective.
```
```
linear load :
  explicit load : 1.2.1.3 [ConfigurationOfPier]
  explicit load : 1.2.1.3 [ConfigurationOfPier]
  linear load : 1.2.1.3 [ConfigurationOfPier]
    explicit load : 1.2.1.4 [ConfigurationOfMagritte]
    linear load : 1.2.1.4 [ConfigurationOfMagritte]
      explicit load : 2.8.4.3 [ConfigurationOfSeaside28]
      load : Magritte-Model-lr.367
      load : Magritte-Seaside-lr.316
    linear load : 1.2.1.4 [ConfigurationOfMagritte]
    load : Pier-Model-lr.351
    load : Pier-Tests-lr.150
    load : Pier-Seaside-lr.451
    load : Pier-Security-lr.144
    load : Pier-Blog-lr.134
    load : Pier-Squeak-Persistency-kph.24
```