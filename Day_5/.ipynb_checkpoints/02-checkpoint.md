<h1>Git Remote Operations</h1>

<h2>List Remote Connections</h2>
<p><code>git remote</code> will list the remote connections you have.</p>
<p><code>git remote -v</code> will list the remote connections along with their URL.</p>

<h2>Add or Remove Remote Repositories</h2>
<p><code>git remote add &lt;name&gt; &lt;url&gt;</code></p>
<p>Adds a new remote repository with the specified name and URL.</p>
<p><code>git remote rm &lt;name&gt;</code></p>
<p>Removes the remote repository with the specified name.</p>

<h2>Hiding Files</h2>
<p>Create a file called <code>.gitignore</code> at the root of the Git repository, then define patterns:</p>
<p><code>Mypasswords.txt</code></p>
<p>- Ignores this specific file</p>
<p><code>directory_name/</code></p>
<p>- Ignores everything in this directory</p>
<p><code>*.sql</code></p>
<p>- Ignores anything ending with .sql</p>

<h2>VS Code</h2>
<p>Accounts > Turn on settings > Sign in > github</p>
<p>Source control > Here we can directly commit</p>
<p>Three dots > Add remote > Add repo link with token</p>
