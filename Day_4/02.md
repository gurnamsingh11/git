<h1>Git Checkout and Detached Head</h1>

<h2>Git Checkout</h2>
<p>The <code>git checkout</code> command allows you to switch between different branches and commits. It can be used to explore historical commits or switch between branches. Here's a basic usage:</p>
<pre>
git checkout branch_name  # Switch to a branch
git checkout <commit>     # Switch to a specific commit
</pre>
<p>To view commit hashes, use:</p>
<pre>
git log --oneline
</pre>

<h2>Detached HEAD State</h2>
<p>When you check out a specific commit, Git places you in a <strong>detached HEAD</strong> state. In this state, you are not on any branch. You can explore and make changes, but any commits made here will not affect the current branches. To create a new branch from this state, use:</p>
<pre>
git switch -c <new-branch-name>
</pre>
<p>To return to your previous branch, use:</p>
<pre>
git switch -
</pre>

<h2>Example</h2>
<p>In the example below, we initialize a Git repository, make several commits, and then use <code>git checkout</code> to explore a previous commit:</p>
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

sagemaker-user@default:~/GIT/Day_4$ git checkout e70fad3
Note: switching to 'e70fad3'.
You are in 'detached HEAD' state. You can look around, make experimental changes and commit them, and you can discard any commits you make in this state without impacting any branches by switching back to a branch.

sagemaker-user@default:~/GIT/Day_4$ git log
commit e70fad38f18d05a332e08f4b09ab9644eeaa0153 (HEAD)
Author: Gurnam <lohiagurunam11@gmail.com>
Date:   Fri Sep 13 19:33:48 2024 +0000

    second commit

commit dc1b826d07671f787dc1da8292b8aa9fd3d20515
Author: Gurnam <lohiagurunam11@gmail.com>
Date:   Fri Sep 13 19:33:15 2024 +0000

    first commit

sagemaker-user@default:~/GIT/Day_4$ git checkout master
Switched to branch 'master'
sagemaker-user@default:~/GIT/Day_4$ git log --oneline
47b9dc8 (HEAD -> master) third commit
e70fad3 second commit
dc1b826 first commit
</pre>
