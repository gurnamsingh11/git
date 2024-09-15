<h1>Add and Commit</h1>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git status</code></p>
<p>On branch master</p>
<p>No commits yet</p>
<p>Untracked files:</p>
<p>(use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>../Day_0/</p>
<p>../Day_1/</p>
<p>./</p>
<p>../git-course/</p>
<p>../private-repo/</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git init</code></p>
<p>Initialized empty Git repository in /home/sagemaker-user/GIT/Day_2/.git/</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git status</code></p>
<p>On branch master</p>
<p>No commits yet</p>
<p>Untracked files:</p>
<p>(use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>.ipynb_checkpoints/</p>
<p>Add_and_Commit.txt</p>
<p>file_one.txt</p>
<p>starting_with_git.txt</p>
<p>untitled.txt</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git add file_one.txt</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git status</code></p>
<p>On branch master</p>
<p>No commits yet</p>
<p>Changes to be committed:</p>
<p>(use "git rm --cached &lt;file&gt;..." to unstage)</p>
<p>new file:   file_one.txt</p>
<p>Untracked files:</p>
<p>(use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>.ipynb_checkpoints/</p>
<p>Add_and_Commit.txt</p>
<p>starting_with_git.txt</p>
<p>untitled.txt</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git commit -m "added first file"</code></p>
<p>[master (root-commit) b196acc] added first file</p>
<p>1 file changed, 1 insertion(+)</p>
<p>create mode 100644 file_one.txt</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git add file_three.txt file_two.txt</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git status</code></p>
<p>On branch master</p>
<p>Changes to be committed:</p>
<p>(use "git restore --staged &lt;file&gt;..." to unstage)</p>
<p>new file:   file_three.txt</p>
<p>new file:   file_two.txt</p>
<p>Untracked files:</p>
<p>(use "git add &lt;file&gt;..." to include in what will be committed)</p>
<p>.ipynb_checkpoints/</p>
<p>Add_and_Commit.txt</p>
<p>starting_with_git.txt</p>
<p>untitled.txt</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git commit -m "Added two files"</code></p>
<p>[master 123b937] Added two files</p>
<p>2 files changed, 2 insertions(+)</p>
<p>create mode 100644 file_three.txt</p>
<p>create mode 100644 file_two.txt</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git add .</code></p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git status</code></p>
<p>On branch master</p>
<p>Changes to be committed:</p>
<p>(use "git restore --staged &lt;file&gt;..." to unstage)</p>
<p>new file:   .ipynb_checkpoints/Add_and_Commit-checkpoint.txt</p>
<p>new file:   .ipynb_checkpoints/file_one-checkpoint.txt</p>
<p>new file:   .ipynb_checkpoints/file_three-checkpoint.txt</p>
<p>new file:   .ipynb_checkpoints/file_two-checkpoint.txt</p>
<p>new file:   .ipynb_checkpoints/starting_with_git-checkpoint.txt</p>
<p>new file:   Add_and_Commit.txt</p>
<p>new file:   starting_with_git.txt</p>
<p>new file:   untitled.txt</p>

<p><code>sagemaker-user@default:~/GIT/Day_2$ git commit -m "Added all files"</code></p>
<p>[master 33641a5] Added all files</p>
<p>8 files changed, 42 insertions(+)</p>
<p>create mode 100644 .ipynb_checkpoints/Add_and_Commit-checkpoint.txt</p>
<p>create mode 100644 .ipynb_checkpoints/file_one-checkpoint.txt</p>
<p>create mode 100644 .ipynb_checkpoints/file_three-checkpoint.txt</p>
<p>create mode 100644 .ipynb_checkpoints/file_two-checkpoint.txt</p>
<p>create mode 100644 .ipynb_checkpoints/starting_with_git-checkpoint.txt</p>
<p>create mode 100644 Add_and_Commit.txt</p>
<p>create mode 100644 starting_with_git.txt</p>
<p>create mode 100644 untitled.txt</p>