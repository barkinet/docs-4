---
title: "Using Snyk with Gradle managed projects"
---
While Snyk does not currently have direct support for projects whose dependencies are managed by [Gradle](https://gradle.org/), it is possible for Snyk to monitor Gradle applications using the [Gradle Maven plugin](https://docs.gradle.org/current/userguide/maven_plugin.html).

Here are the steps you'll need to take:

<ol>
<li>Add the Gradle Maven Plugin to your <code>build.gradle</code> file by including the following line:

<pre class=" language-console"><code class="language-console language-js" data-lang="console">apply plugin: 'maven'</code></pre>
</li>

<li>Run <code>./gradlew install</code>. This will install the associated artifacts to the local Maven cache (<code>~/.m2</code>).</li>

<li>After running <code>install</code>, a new Maven-style pom file will be created in <code>build/poms/pom-default.xml</code>. Copy that file to the root directory:

<pre class=" language-console"><code class="language-console" data-lang="console">$ cp build/poms/pom-default.xml pom.xml</code></pre>
</li>
</ol>

You should now have a `pom.xml` file that Snyk can test against. Now if you try to test the project with Snyk from the [CLI](/docs/using-snyk/), or by using the [GitHub integration](/docs/github), Snyk will see the `pom.xml` and test it as if it was a Maven-based project.
