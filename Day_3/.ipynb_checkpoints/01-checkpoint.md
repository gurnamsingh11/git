<h1>Git Branch Commands</h1>
<h2>Create a New Repo</h2>
<p><code>git branch &lt;branch_name&gt;</code></p>

<h2>Report Branches</h2>
<p><code>git branch</code></p>

<h2>Switch Branches</h2>
<p><code>git switch</code></p>

<h2>Example Commands and Outputs</h2>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch master

No commits yet

Untracked files:
  (use "git add &lt;file&gt;..." to include in what will be committed)
        ../Day_0/
        ../Day_1/
        ../Day_2/
        ./
        ../git-course/
        ../private-repo/
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git init</code></p>
<pre>
Initialized empty Git repository in /home/sagemaker-user/GIT/Day_3/.git/
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
fatal: your current branch 'master' does not have any commits yet
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "My First commiy"</code></p>
<pre>
[master (root-commit) 67df12e] My First commiy
 1 file changed, 3 insertions(+)
 create mode 100644 my_file.txt
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit 67df12e0f31ee9baf35a9e6387b2e112c6784bef (HEAD -> master)

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch</code></p>
<pre>
* master
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch new_branch</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch</code></p>
<pre>
* master
  new_branch
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "Added new line"</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit 9b3a97ba2cf2102981373accc308e315e38a279a (HEAD -> master)

    Added new line

commit 67df12e0f31ee9baf35a9e6387b2e112c6784bef (new_branch)

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch new_branch</code></p>
<pre>
Switched to branch 'new_branch'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit 67df12e0f31ee9baf35a9e6387b2e112c6784bef (HEAD -> new_branch)

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch new_branch

nothing added to commit but untracked files present (use "git add" to track)
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch new_branch
Changes not staged for commit:
  (use "git add &lt;file&gt;..." to update what will be committed)
  (use "git restore &lt;file&gt;..." to discard changes in working directory)
        modified:   my_file.txt

Untracked files:
  (use "git add &lt;file&gt;..." to include in what will be committed)
        .ipynb_checkpoints/
        Git-Branch-Commands.txt

no changes added to commit (use "git add" and/or "git commit -a")
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "new updates for new branch"</code></p>
<pre>
[new_branch f792bf8] new updates for new branch
 1 file changed, 2 insertions(+), 1 deletion(-)
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit f792bf8e034dd3768e7450e0c651e49ac060175f (HEAD -> new_branch)

    new updates for new branch

commit 67df12e0f31ee9baf35a9e6387b2e112c6784bef (new_branch)

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch master</code></p>
<pre>
Switched to branch 'master'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit 9b3a97ba2cf2102981373accc308e315e38a279a (HEAD -> master)

    Added new line

commit 67df12e0f31ee9baf35a9e6387b2e112c6784bef

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch new_branch</code></p>
<pre>
Switched to branch 'new_branch'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch</code></p>
<pre>
  master
* new_branch
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch experimenal</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch experimenal</code></p>
<pre>
Switched to branch 'experimenal'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch experimenal
Changes not staged for commit:
  (use "git add &lt;file&gt;..." to update what will be committed)
  (use "git restore &lt;file&gt;..." to discard changes in working directory)
        modified:   my_file.txt

Untracked files:
  (use "git add &lt;file&gt;..." to include in what will be committed)
        .ipynb_checkpoints/
        Git-Branch-Commands.txt

no changes added to commit (use "git add" and/or "git commit -a")
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "Experimental updates"</code></p>
<pre>
[experimenal 1dd002e] Experimental updates
 1 file changed, 2 insertions(+), 1 deletion(-)
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit 1dd002e309c44491747b084959eb98839c3643fb (HEAD -> experimenal)

    Experimental updates

commit f792bf8e034dd3768e7450e0c651e49ac060175f (new_branch)

    new updates for new branch

commit 67df12e0f31ee9baf35a9e6387b2e112c6784bef

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch experimenal
Untracked files:
  (use "git add &lt;file&gt;..." to include in what will be committed)
        .ipynb_checkpoints/
        Git-Branch-Commands.txt

nothing added to commit but untracked files present (use "git add" to track)
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch new_branch</code></p>
<pre>
Switched to branch 'new_branch'
</pre>
