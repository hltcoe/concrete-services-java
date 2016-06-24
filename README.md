Copyright 2012-2015 Johns Hopkins University HLTCOE. All rights
reserved.  This software is released under the 2-clause BSD license.
See LICENSE in the project root directory.

Concrete Core
========
![Maven Badges](https://maven-badges.herokuapp.com/maven-central/edu.jhu.hlt/concrete-core/badge.svg)
[![javadoc.io](https://javadocio-badges.herokuapp.com/edu.jhu.hlt/concrete-core/badge.svg)](http://www.javadoc.io/doc/edu.jhu.hlt/concrete-core/)

Provides Java classes for the [Concrete](https://github.com/hltcoe/concrete) HLT data schema.

Maven dependency
---
```xml
<dependency>
  <groupId>edu.jhu.hlt</groupId>
  <artifactId>concrete-services-core</artifactId>
  <version>x.y.z</version>
</dependency>
```

Requirements
------------

Concrete Core requires the following:
* Java, 1.6 or greater.
* [Apache Maven](http://maven.apache.org/), 3.0.4 or greater
* [Apache Thrift](http://thrift.apache.org/), 0.9.1
* `bash` shell

Installation (*nix only)
------------

Concrete requires `bash` and `thrift` installed and available on your `PATH`.

Additionally, you will need a copy of `concrete-thrift` checked
out. This repository can be closed in *nix via:


```bash
git clone git@github.com:hltcoe/concrete.git
```

Next, set the environment variable `PATH_TO_CONCRETE_FILES`
to the path where the concrete `.thrift` files exist on disk. For example,
if you just cloned the project per above, this would be `concrete/thrift`.

Next, set the environment variable `PATH_TO_CONCRETE_SERVICES_FILES`
to the path where the concrete services`.thrift` files exist on disk. For example,
if you just cloned the project, this would be `$(pwd)/concrete-services-core/thrift`.

You also need a `jdk` version `1.6` installed. This is necessary
to support some legacy pipelines and projects. Set `JAVA_1_6_HOME`
to the path of JDK1.6.

Afterwards, running:

```sh
mvn install
```

will install the code to your local maven repository.

Using the code in your project
------------------------------

Compiled java classes end up in the edu.jhu.hlt.concrete package. The
Thrift structures generate many classes; additional technical
documentation can be found in the comments of the thrift definitions
themselves, or in the Javadocs.
