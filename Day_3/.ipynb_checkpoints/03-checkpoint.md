<h1>Merging Branches</h1>

<h2>Initializing a Repository</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git init</code></p>
<pre>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: 
hint:   git config --global init.defaultBranch &lt;name&gt;
hint: 
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 
hint:   git branch -m &lt;name&gt;
Initialized empty Git repository in /home/sagemaker-user/GIT/Day_3/.git/
</pre>

<h2>Committing Changes</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "added myfile"</code></p>
<pre>
[master (root-commit) bc4a6a4] added myfile
 1 file changed, 1 insertion(+)
 create mode 100644 my_file.txt
</pre>

<h2>Creating and Switching Branches</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch new_branch</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch new_branch</code></p>

<h2>Making Commits in New Branch</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "added new branch line"</code></p>
<pre>
[new_branch 1768d7c] added new branch line
 1 file changed, 2 insertions(+), 1 deletion(-)
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "yet another line"</code></p>
<pre>
[new_branch f2eb752] yet another line
 1 file changed, 2 insertions(+), 1 deletion(-)
</pre>

<h2>Switching Back to Master and Merging</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch master</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git merge new_branch</code></p>
<pre>
Updating bc4a6a4..f2eb752
Fast-forward
 my_file.txt | 4 +++-
 1 file changed, 3 insertions(+), 1 deletion(-)
</pre>

<h2>Creating and Switching to New Branches</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch experimental</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch experimental</code></p>

<h2>Committing Changes in Experimental Branch</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git add experimental.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "added experimental.txt"</code></p>
<pre>
[experimental 13de7ea] added experimental.txt
 1 file changed, 1 insertion(+)
 create mode 100644 experimental.txt
</pre>

<h2>Merging Experimental Branch into Master</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch master</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git merge experimental</code></p>
<pre>
Merge made by the 'ort' strategy.
 experimental.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 experimental.txt
</pre>

<h2>Creating and Switching to Bug QA Branch</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git branch bug_qa</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch bug_qa</code></p>

<h2>Committing Changes in Bug QA Branch</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "qa bug test code on line four"</code></p>
<pre>
[bug_qa f7df06f] qa bug test code on line four
 1 file changed, 2 insertions(+), 1 deletion(-)
</pre>

<h2>Merging Bug QA Branch into Master</h2>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git switch master</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git merge bug_qa</code></p>
<pre>
Auto-merging my_file.txt
CONFLICT (content): Merge conflict in my_file.txt
Automatic merge failed; fix conflicts and then commit the result.
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_3$ git commit -m "fixed conflicts"</code></p>
<pre>
[master 49b0575] fixed conflicts
</pre>

<p><code>sagemaker-user@default:~/GIT/Day_3$ git status</code></p>
<pre>
On branch master
Untracked files:
  (use "git add &lt;file&gt;..." to include in what will be committed)
        .ipynb_checkpoints/
        01_Git-Branch-Commands.txt
        02_Delete-Rename-Branches.txt
        03_Merging-Branches.txt

nothing added to commit but untracked files present (use "git add" to track)
</pre>
