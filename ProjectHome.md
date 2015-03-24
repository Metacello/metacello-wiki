Metacello is a package management system for Monticello that is consistent with the important features of Monticello:
  * Declarative modeling. A Metacello project has named versions consisting of lists of explicit Monticello package versions. Dependencies are explicitly expressed in terms of named versions of required projects. A required project is a reference to another Metacello project.
  * Distributed repositories. Metacello project metadata is represented as instance methods in a class therefore the Metacello project metadata is stored in a Monticello package. As a result, it is easy for distributed groups of developers to collaborate on ad hoc projects.
  * Optimistic development. With Monticello-based packages, concurrent updates to the project metadata can be easily managed. Parallel versions of the metadata can be merged just like parallel versions of the code base itself.

Additionally, the following three points are important considerations for Metacello:

  * Cross platform operation. Metacello must run on all platforms that support Monticello: currently Squeak, Pharo and GLASS.
  * Conditional Monticello package loading. For projects that are expected to run on multiple platforms, it is essential that platform-specific Monticello packages can be conditionally loaded.


---


[Download instructions](DownloadMetacello.md).


---


Be sure to the check out the ProfStef tutorial with step by step instructions for creating a Metacello configuration:
```
(ConfigurationOfMetacello project version: #stable) load: #('Tutorial').
ProfStef goOn: MetacelloDevelopmentProcess.
```
If you don't have access to ProfStef, follow [these steps](CreateMetacelloConfiguration.md).


---


  * [Installation instructions](DownloadMetacello.md)
  * [Loading projects and building your own images with Metacello](http://marianopeck.wordpress.com/2011/11/19/loading-projects-and-building-your-own-images-with-metacello/)
  * [Metacello Toolbox](http://seandenigris.com/blog/?p=844).
  * Everything you wanted to Know About Metacello (But Were Afraid to Ask)
    * ESUG 2010 (Dale Henrichs and Mariano Martinez-Peck)
      * [slides](http://www.slideshare.net/esug/metacello-esug2010) and [video](http://www.youtube.com/watch?v=zWHS5xIo_xI&feature=youtu.be&a)
    * Smalltalks 2010 (Mariano Martinez-Peck)
      * [video](http://www.fast.org.ar/smalltalks2010/videos/Metacello)
  * [(gem)Stone Soup posts on Metacello](http://gemstonesoup.wordpress.com/category/metacello/)
  * [MetacelloBrowser for Pharo](http://www.squeaksource.com/MetacelloBrowser.html)
  * [Pharo cast: Introduction to Monticello and Metacello](http://www.pharocasts.com/2010/07/monticello-and-metacello-introduction.html)
  * [Why a Package Management System?](http://code.google.com/p/metacello/wiki/WhyAPackageManagementSystem) - Torsten Bergmann provides a fairly complete use case for Metacello
  * [Metacello Bug Reports](http://code.google.com/p/metacello/issues/list)
  * [Creating a Metacello Configuration](CreateMetacelloConfiguration.md)
  * [Tutorial](Tutorial.md)
  * Fetch and Record
    * [Determining which mcz files will be loaded](DeterminingWhichMCZFileWillBeLoaded.md)
    * [Programmatic fetch/load](ProgrammaticFetchLoad.md)
    * [Maintaining a secondary repository for Metacello](MaintainingSecondaryRepository.md)
    * [Using a local directory repository](UsingLocalDirectoryRepository.md)
  * [Mailing list](http://groups.google.com/group/metacello)
  * [API reference](APIReference.md)
  * [FAQ](FAQ.md)
  * [Tool docs](MetacelloTools.md)
  * [Pharo Metacello Configurations Repository](http://www.squeaksource.com/MetacelloRepository.html) (excellent source of example configurations)
