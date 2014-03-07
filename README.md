maven-local-deployer [![Build Status](https://travis-ci.org/ichigotake/maven-local-deployer.png?branch=ci-test)](https://travis-ci.org/ichigotake/maven-local-deployer)
==========

Add `uploadArchives` task for upload maven repository to local file system.

Usage
----------

``` groovy
// I recommend to don't use direct url, and cache this (e.g. git submodule).
apply from: 'https://raw.github.com/ichigotake/maven-local-deployer/master/build.gradle'

def repositoryDir = project.projectDir.getAbsolutePath() + '/repository';
def mavenConfig = [
        groupId: 'net.ichigotake.maven_local_deployer',
        artifactId: 'test-library',
        versionName: '0.1.2',
]

mavenLocalDeployer(repositoryDir, mavenConfig)

```

License
----------

[Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0)
