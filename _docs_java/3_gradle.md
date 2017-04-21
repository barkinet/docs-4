---
title: "Using Snyk with Gradle managed projects"
---
While Snyk does not currently have direct support for projects whose dependencies are managed by [Gradle](https://gradle.org/), it is possible for Snyk to monitor Gradle applications using the [Gradle Maven plugin](https://docs.gradle.org/current/userguide/maven_plugin.html).

Here are the steps you'll need to take:

1. Add the Gradle Maven Plugin to your `build.gradle` file by including the following line:

```
apply plugin: 'maven'
```

2. Run `./gradlew install`. This will install the associated artificats to the local Maven cache (`~/.m2`).
3. After running `install`, a new Maven-style pom file will be created in `build/poms/pom-default.xml`. Copy that file to the root directory:

```
$ cp build/poms/pom-default.xml pom.xml
```

You should now have a `pom.xml` file that Snyk can test against. Now if you try to test the project with Snyk from the [CLI](/docs/using-snyk/), or by using the [GitHub integration](/docs/github), Snyk will see the `pom.xml` and test it as if it was a Maven-based project.