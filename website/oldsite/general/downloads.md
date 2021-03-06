---
layout: default
title: Downloads
theme:
    name: retro-mahout
---

<a name="Downloads-OfficialRelease"></a>
# Official Release
Apache Mahout is an official Apache project and thus available from any of
the Apache mirrors. The latest Mahout release is available for download at: 

* [Download Latest](http://www.apache.org/dyn/closer.cgi/mahout/)
* [Release Archive](http://archive.apache.org/dist/mahout/)


# Source code for the current snapshot

Apache Mahout is mirrored to [Github](https://github.com/apache/mahout). To get all source:

    git clone https://github.com/apache/mahout.git mahout
   
# Environment

Whether you are using Mahout's Shell, running command line jobs or using it as a library to build your own apps 
you'll need to setup several environment variables. 
Edit your environment in ```~/.bash_profile``` for Mac or ```~/.bashrc``` for many linux distributions. Add the following

    export MAHOUT_HOME=/path/to/mahout
    export MAHOUT_LOCAL=true # for running standalone on your dev machine, 
    # unset MAHOUT_LOCAL for running on a cluster 

If you are running on Spark you will also need $SPARK_HOME

Make sure to have $JAVA_HOME set also

# Using Mahout as a Library

Running any application that uses Mahout will require installing a binary or source version and setting the environment.  
Then add the appropriate setting to your pom.xml or build.sbt following the template below.
 
If you only need the math part of Mahout:

    <dependency>
        <groupId>org.apache.mahout</groupId>
        <artifactId>mahout-math</artifactId>
        <version>${mahout.version}</version>
    </dependency>

In case you would like to use some of our integration tooling (e.g. for generating vectors from Lucene):

    <dependency>
        <groupId>org.apache.mahout</groupId>
        <artifactId>mahout-hdfs</artifactId>
        <version>${mahout.version}</version>
    </dependency>

In case you are using Ivy, Gradle, Buildr, Grape or SBT you might want to directly head over to the official [Maven Repository search](http://mvnrepository.com/artifact/org.apache.mahout/mahout-core).


<a name="Downloads-FutureReleases"></a>
# Future Releases

Official releases are usually created when the developers feel there are
sufficient changes, improvements and bug fixes to warrant a release. Watch
the <a href="https://mahout.apache.org/general/mailing-lists,-irc-and-archives.html">Mailing lists</a>
 for latest release discussions and check the Github repo.

