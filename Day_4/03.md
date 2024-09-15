<h1>Git Restore</h1>

<h2>Restoring Files to a Previous Commit</h2>
<p>The <code>git restore</code> command allows you to restore files to their state at a specific commit. This can be useful if you want to undo changes in a file or restore a file from a previous commit:</p>
<pre>
git restore file_name
</pre>
<p>To restore a file from a specific commit, use:</p>
<pre>
git restore --source HEAD~N file.txt
</pre>
<p>Here, <code>~N</code> specifies the number of commits prior to HEAD that you want to go back to.</p>

<h2>Unstaging Files</h2>
<p>You can also use <code>git restore</code> to unstage files that have been added to the staging area with <code>git add</code>:</p>
<pre>
git restore --staged filename
</pre>

<h2>Example</h2>
<p>In the example below, we initialize a Git repository, make several commits, and use <code>git restore</code> to revert files and unstage changes:</p>
<pre>
sagemaker-user@default:~/GIT/Day_4$ git init
Initialized empty Git repository in /home/sagemaker-user/GIT/Day_4/.git/

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "first commit"
[master (root-commit) dc1b826] first commit
 1 file changed, 1 insertion(+)

sagemaker-user@default:~/GIT/Day_4$ git commit -m "second commit"
[master e70fad3] second commit
 1 file changed, 2 insertions(+), 1 deletion(-)

sagemaker-user@default:~/GIT/Day_4$ git commit -m "third commit"
[master 47b9dc8] third commit
 1 file changed, 2 insertions(+), 1 deletion(-)

sagemaker-user@default:~/GIT/Day_4$ git log --oneline
47b9dc8 (HEAD -> master) third commit
e70fad3 second commit
dc1b826 first commit

sagemaker-user@default:~/GIT/Day_4$ git restore myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git log --oneline
47b9dc8 (HEAD -> master) third commit
e70fad3 second commit
dc1b826 first commit

sagemaker-user@default:~/GIT/Day_4$ git restore --source HEAD~2 myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   myfile.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .ipynb_checkpoints/
        01_undergoing_changes.txt
        02_Git-Checkout-and-Detached-Head.txt
        03_Git-Restore.txt

no changes added to commit (use "git add" and/or "git commit -a")

sagemaker-user@default:~/GIT/Day_4$ git add code.txt mynotes.txt
sagemaker-user@default:~/GIT/Day_4$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   code.txt
        new file:   mynotes.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   myfile.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .ipynb_checkpoints/
        01_undergoing_changes.txt
        02_Git-Checkout-and-Detached-Head.txt
        03_Git-Restore.txt
        mynotes.txt

sagemaker-user@default:~/GIT/Day_4$ git restore --staged mynotes.txt
sagemaker-user@default:~/GIT/Day_4$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   code.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   myfile.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .ipynb_checkpoints/
        01_undergoing_changes.txt
        02_Git-Checkout-and-Detached-Head.txt
        03_Git-Restore.txt
        mynotes.txt
</pre>
