<h1>Git Commands</h1>

<h2>Initialize Git Repository</h2>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git init</code></p>
<p>hint: Using 'master' as the name for the initial branch. This default branch name</p>
<p>hint: is subject to change. To configure the initial branch name to use in all</p>
<p>hint: of your new repositories, which will suppress this warning, call:</p>
<p>hint:</p>
<p>hint:   <code>git config --global init.defaultBranch &lt;name&gt;</code></p>
<p>hint:</p>
<p>hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and</p>
<p>hint: 'development'. The just-created branch can be renamed via this command:</p>
<p>hint:</p>
<p>hint:   <code>git branch -m &lt;name&gt;</code></p>
<p>Initialized empty Git repository in /home/sagemaker-user/GIT/Day_5/.git/</p>

<h2>Add and Commit Files</h2>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git add master.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git commit -m "first commit on master"</code></p>
<p>[master (root-commit) 781d005] first commit on master</p>
<p> 1 file changed, 1 insertion(+)</p>
<p> create mode 100644 master.txt</p>

<h2>Create and Switch Branches</h2>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git branch other</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git branch</code></p>
<p>* master</p>
<p>  other</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch other</code></p>
<p>Switched to branch 'other'</p>

<h2>Check Status on Branches</h2>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git status</code></p>
<p>On branch other</p>
<p>Untracked files:</p>
<p>  (use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>        .ipynb_checkpoints/</p>
<p>        01_Git-Stash.txt</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<p><code>sagemaker-user@default:~/GIT/Day_5$ git status</code></p>
<p>On branch other</p>
<p>Untracked files:</p>
<p>  (use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>        .ipynb_checkpoints/</p>
<p>        01_Git-Stash.txt</p>
<p>        other.txt</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch master</code></p>
<p>Switched to branch 'master'</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git status</code></p>
<p>On branch master</p>
<p>Untracked files:</p>
<p>  (use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>        .ipynb_checkpoints/</p>
<p>        01_Git-Stash.txt</p>
<p>        other.txt</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<h2>Stash Changes</h2>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch other</code></p>
<p>Switched to branch 'other'</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git add other.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git commit -m "other commit"</code></p>
<p>[other b57b111] other commit</p>
<p> 1 file changed, 1 insertion(+)</p>
<p> create mode 100644 other.txt</p>

<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch master</code></p>
<p>M       master.txt</p>
<p>Switched to branch 'master'</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch other</code></p>
<p>M       master.txt</p>
<p>Switched to branch 'other'</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git stash</code></p>
<p>Saved working directory and index state WIP on other: b57b111 other commit</p>

<h2>Apply Stashed Changes</h2>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch master</code></p>
<p>Switched to branch 'master'</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git add master.txt</code></p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git commit -m "updated master.txt"</code></p>
<p>[master 717d876] updated master.txt</p>
<p> 1 file changed, 2 insertions(+), 1 deletion(-)</p>

<p><code>sagemaker-user@default:~/GIT/Day_5$ git switch other</code></p>
<p>Switched to branch 'other'</p>
<p><code>sagemaker-user@default:~/GIT/Day_5$ git stash pop</code></p>
<p>On branch other</p>
<p>Changes not staged for commit:</p>
<p>  (use "git add &lt;file&gt;..." to update what will be committed)</p>
<p>  (use "git restore &lt;file&gt;..." to discard changes in working directory)</p>
<p>        modified:   master.txt</p>
<p>Untracked files:</p>
<p>  (use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>        .ipynb_checkpoints/</p>
<p>        01_Git-Stash.txt</p>
<p>no changes added to commit (use "git add" and/or "git commit -a")</p>
<p>Dropped refs/stash@{0} (de8d34a1417ef94f09d88eb953b7e1e66376ea41)</p>
