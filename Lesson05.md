|see [version05:](Version05.md)|[Answer05](Answer05.md)|[Answer06](Answer06.md)|[Answer07](Answer07.md)|[Answer08](Answer08.md)|
|:-----------------------------|:----------------------|:----------------------|:----------------------|:----------------------|

For version 0.5 we've added an additional package to the mix: 'Example-AddOn':

> [(MetacelloTutorialConfig project version: '0.5') spec.](Answer05.md)

Of course, the point of specifiying packages in Metacello is to be able to load versions. Here are
a couple examples of loading versions of the Tutorial. If you print the result of each expression,
you will see the list of packages in load order (note that for the tutorial, we are using the
MetacelloNullRecordingMCSpecLoader. This class records which packages are loaded and the order that they are loaded in among other things instead of actually loading the packages.

> [(MetacelloTutorialConfig project version: '0.1') load.](Answer06.md)

> [(MetacelloTutorialConfig project version: '0.4') load.](Answer06.md)

> [(MetacelloTutorialConfig project version: '0.5') load.](Answer06.md)

You will note that in each case, all of the packages associated with the version are loaded, which
is the default.

If you want to load a subset of the packages in a project, you may list the packages that you
are interested in as an argument to the #load: method:

> [(MetacelloTutorialConfig project version: '0.5') load: { 'Example-Tests'. 'Example-Core' }.](Answer07.md)

Note that the ordering of the packages is based on the order in which the packages are specified.

If you evaluate the following expression:

> [(MetacelloTutorialConfig project version: '0.5') load: { 'Example-Tests'. }.](Answer08.md)

Only the package is 'Example-Tests'. By default the packages are ordered, but there are no implicit
dependencies.
|[Lesson 6](Lesson06.md)|
|:----------------------|