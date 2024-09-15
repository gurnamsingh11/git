<h1>Git Remote and Git Push</h1>

<p>We can check for remote branches with the command:</p>
<p><code>git remote -v</code></p>

<p>If you run this command on a cloned repo, you will view the URL of the remote branch, like the Github URL.</p>
<p>If there is no connection to a remote branch, then you won't see a URL.</p>

<p>After creating a repo locally, we need to create the repo on Github.</p>
<p>Once created the repo on Github, you will see the instructions under: ".. or push an existing repo from command line"</p>

<p>We tell git we want to add a remote branch using <code>git remote</code>:</p>
<p><code>git remote add name https://url.git</code></p>

<p>By convention, we call this remote branch the origin branch:</p>
<p><code>git remote add origin https://url.git</code></p>

<p>You then replace the .git URL with the .git URL from the repo you created.</p>

<p>Few commands:</p>
<p><code>git remote rename &lt;old&gt; &lt;new&gt;</code></p>
<p><code>git remote remove &lt;name&gt;</code></p>

<p>Push:</p>
<p>We tell git to push to the remote main/master branch called origin with the command:</p>
<p><code>git push -u origin main/master</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git remote -v</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_2$ git remote add origin https://token@github.com/gurnamsingh11/Learn_git.git</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_2$ git push -u origin master</code></p>
<p>done.</p>
<p>To https://github.com/gurnamsingh11/Learn_git.git</p>
<p>* [new branch]      master -> master</p>
<p>Branch 'master' set up to track remote branch 'master' from 'origin'.</p>
