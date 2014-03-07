maven-local-deployer [![Build Status](https://travis-ci.org/ichigotake/gradle-maven-local-deployer.png?branch=master)](https://travis-ci.org/ichigotake/gradle-maven-local-deployer)
==========

Add `uploadArchives` task for upload maven repository to local file system.

Usage
----------

``` groovy
// I recommend to don't use direct url, and cache this (e.g. git submodule).
apply from: 'https://raw.github.com/ichigotake/gradle-maven-local-deployer/master/build.gradle'

def repositoryDir = project.projectDir.getAbsolutePath() + '/repository';
def mavenConfig = [
        groupId: 'net.ichigotake.maven_local_deployer',
        artifactId: 'test-library',
        version: '0.1.2',
]

mavenLocalDeployer(repositoryDir, mavenConfig)

// Run task
// $ ./gradlew :library:uploadArchives

```

License
----------

[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
