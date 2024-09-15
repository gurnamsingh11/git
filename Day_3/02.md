<h1>Delete-Rename-Branches</h1>

<h2>Renaming a Branch</h2>
<p><code>git switch &lt;branch_to_rename&gt;</code></p>
<p><code>git branch -m &lt;new_name&gt;</code></p>

<h2>Deleting a Branch</h2>
<p><code>git branch -d &lt;branch_to_delete_name&gt;</code></p>

<h2>Example Commands and Outputs</h2>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch new_branch
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch master</code></p>
<pre>
Switched to branch 'master'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch experimenal</code></p>
<pre>
Switched to branch 'experimenal'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch -m please_delete</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch please_delete
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git log</code></p>
<pre>
commit 1dd002e309c44491747b084959eb98839c3643fb (HEAD -> please_delete)

    Experimental updates

commit f792bf8e034dd3768e7450e0c651e49ac060175f (new_branch)

    new updates for new branch

    My First commiy
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch master</code></p>
<pre>
Switched to branch 'master'
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch -d please_delete</code></p>
<pre>
error: The branch 'please_delete' is not fully merged.

If you are sure you want to delete it, run 'git branch -D please_delete'.
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch -D please_delete</code></p>
<pre>
Deleted branch please_delete (was 1dd002e).
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch</code></p>
<pre>
* master
  new_branch
</pre>
