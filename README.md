JHOVE
=====

This is a small project to take the JHOVE source code and Mavenise it, so that snapshots and official releases can be published.

jhove-releases
--------------
This is a pom that can be used to build Maven bundles from JHOVE release packages.

jhove-snapshot
--------------
This generates Maven artefacts for JHOVE directly from the HEAD of the CVS repository. It is thus suitable for generating SNAPSHOT builds.

jhove-scj-snapshot
------------------
As jhove-snapshot, but the codebase has been very slightly patched, in JhoveBase, so that JHove will pick up a config file from inside the main JAR if non is supplied. This allows JHove to be run as a standalone JAR.
