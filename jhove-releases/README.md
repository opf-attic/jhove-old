Mavenising JHOVE Releases
=========================

This POM can be used to build code bundles of JHOVE releases. These can then be submitted to Maven central via Sonatype: https://docs.sonatype.org/display/Repository/Uploading+3rd-party+Artifacts+to+Maven+Central

As per those instructions, it's run like this:

mvn source:jar javadoc:jar package gpg:sign repository:bundle-create -Dgpg.passphrase=xxx

When executed, the POM downloads the zip files, unpacks the necessary items and packages them up for Maven. It currently does not includes the extramodules code or the example config files in the JAR.

This does not work for version 1.1, which under Java 6, fails with this error: can't implement pop() in java.util.Deque. This is probably because it uses deprecated Java features, and thus it may be possible to build it under an old Java version.

Not also that because some of the JHOVE classes are in the default package, the POM needs to specify use=false to avoid a known bug during javadoc creation:
http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=6442980
