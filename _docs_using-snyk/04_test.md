---
title: Test
---
<h3>Test a local project</h3>
<p>To only test your project for known vulnerabilities, browse to your project’s folder and run <code>snyk test</code>:</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">cd ~/projects/myproj/</span>
<span class="go">snyk test</span></code></pre></div>

<p><code>snyk test</code> takes stock of all the local dependencies and queries the snyk service for related known vulnerabilities. It displays the found issues along with additional information. For Node.js projects, it also suggests remediation steps.</p>

<p>When <code>snyk test</code> runs, it tries to detect the appropriate file for your project by looking for the following files, in this order:</p>
<ol><li>yarn.lock</li><li>package.json</li><li>Gemfile</li><li>Gemfile.lock</li><li>pom.xml</li></ol>

<p>When testing locally, you can specify the file that Snyk should inspect for package information.</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">$ snyk test --file=package.json</span>
</code></pre></div>

<p><code>snyk test</code> can also get a folder name as an argument, which is especially handy if you want to <strong>test multiple projects.</strong> For instance, the following command tests all the projects under a certain folder for known vulnerabilities:</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">cd ~/projects/</span>
<span class="go">snyk test *</span></code></pre></div>

<p>Note for Node.js: <br>
Since <code>snyk test</code> looks at the locally installed modules, it needs to run after <code>npm install</code> or <code>yarn install</code>, and will seamlessly work with <code>shrinkwrap</code>, npm enterprise or any other custom installation logic you have.</p>

<p>Note for Java: <br>
Since <code>snyk test</code> looks at the locally installed modules, it needs to run after <code>mvn install</code>.</p>

<h3>Test a public GitHub repository</h3>
<p>To test a public Github repository, run <code>snyk test</code> and include the Github URL to the repo.</p>
<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk test https://github.com/snyk/snyk</span></code></pre></div>
<p>The following git URL formats are supported:</p>

<ul>
  <li>git://github.com/user/project.git#commit-ish</li>
  <li>https://github.com/user/project#commit-ish</li>
  <li>user/project#commit-ish</li>
</ul>
<p>This also works for Bitbucket and GitLab.</p>
<p>You can also test a public npm package or Github project <a href="https://snyk.io/test/" title="Test page">via the Test page on snyk.io.</a></p>

<h3>Test a public npm package</h3>
<p>You can also use <code>snyk test</code> to <strong>scrutinize a public package before installing it</strong>, to see if it has known vulnerabilities or not. Using the package name will test the latest version of that package, and you can also provide a specific version or range using <code>snyk test module[@semver-range]</code>.</p>

<div class="highlight"><pre><code class="language-console" data-lang="console"><span class="go">snyk test lodash</span>
<span class="go">snyk test ionic@1.6.5</span></code></pre></div>
