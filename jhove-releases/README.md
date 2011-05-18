 Via

https://docs.sonatype.org/display/Repository/Uploading+3rd-party+Artifacts+to+Maven+Central

1.1 failed
can't implement pop() in java.util.Deque

mvn source:jar javadoc:jar package gpg:sign repository:bundle-create -Dgpg.passphrase=xxx

Had to use use=false to avoid bug in javadoc creation
http://bugs.sun.com/bugdatabase/view_bug.do?bug_id=6442980
