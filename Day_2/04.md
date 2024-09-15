<h1>Fetch and Pull</h1>

<p>We created a new file on GitHub repo</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git fetch</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git checkout origin/master</code></p>
<p>M       .ipynb_checkpoints/Add_and_Commit-checkpoint.txt<br>
D       .ipynb_checkpoints/file_one-checkpoint.txt<br>
D       .ipynb_checkpoints/file_three-checkpoint.txt<br>
D       .ipynb_checkpoints/file_two-checkpoint.txt<br>
M       Add_and_Commit.txt<br>
D       file_one.txt<br>
D       file_three.txt<br>
D       file_two.txt<br>
D       untitled.txt</p>
<p>Note: switching to 'origin/master'.</p>
<p>You are in 'detached HEAD' state. You can look around, make experimental changes and commit them, and you can discard any commits you make in this state without impacting any branches by switching back to a branch.</p>
<p>If you want to create a new branch to retain commits you create, you may do so (now or later) by using -c with the switch command. Example:</p>
<p><code>git switch -c &lt;new-branch-name&gt;</code></p>
<p>Or undo this operation with:</p>
<p><code>git switch -</code></p>
<p>Turn off this advice by setting config variable <code>advice.detachedHead</code> to false</p>
<p>HEAD is now at ed7987f Create brand_new_file.txt</p>
<p>Using the above command, it will show new files created from GitHub to local but temporarily</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git switch master</code></p>
<p>M       .ipynb_checkpoints/Add_and_Commit-checkpoint.txt<br>
D       .ipynb_checkpoints/file_one-checkpoint.txt<br>
D       .ipynb_checkpoints/file_three-checkpoint.txt<br>
D       .ipynb_checkpoints/file_two-checkpoint.txt<br>
M       Add_and_Commit.txt<br>
D       file_one.txt<br>
D       file_three.txt<br>
D       file_two.txt<br>
D       untitled.txt</p>
<p>Previous HEAD position was ed7987f Create brand_new_file.txt<br>
Switched to branch 'master'<br>
Your branch is behind 'origin/master' by 1 commit, and can be fast-forwarded.<br>
  (use "git pull" to update your local branch)</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git pull</code></p>
<p>Updating 33641a5..ed7987f<br>
Fast-forward<br>
 brand_new_file.txt | 1 +<br>
 1 file changed, 1 insertion(+)<br>
 create mode 100644 brand_new_file.txt</p>
<p>Using the above command will get all files to local</p>
