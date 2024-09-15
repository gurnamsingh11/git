<h1>Git Revert</h1>

<h2>Overview</h2>
<p>The <code>git revert</code> command creates a new commit that undoes the changes introduced by a previous commit. This method is useful for reversing changes while preserving the commit history.</p>

<h2>Use Case</h2>
<p>Unlike <code>git reset</code>, which alters the commit history, <code>git revert</code> keeps the commit history intact by adding a new commit that effectively undoes the changes from a specific commit. This is useful when you want to undo changes without rewriting history.</p>

<h2>Examples</h2>
<p>Here’s an example workflow demonstrating how to use <code>git revert</code>:</p>
<pre>
sagemaker-user@default:~/GIT/Day_4$ git init
Initialized empty Git repository in /home/sagemaker-user/GIT/Day_4/.git/

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "good code"
[master (root-commit) c86f7d1] one more line of good code
 1 file changed, 2 insertions(+)

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "buggy commit"
[master c34adb4] buggy commit
 1 file changed, 2 insertions(+), 1 deletion(-)

sagemaker-user@default:~/GIT/Day_4$ git log --oneline
c34adb4 (HEAD -> master) buggy commit
c86f7d1 one more line of good code

sagemaker-user@default:~/GIT/Day_4$ git revert c34adb4
[master e704400] Revert "buggy commit"
 1 file changed, 1 insertion(+), 2 deletions(-)

sagemaker-user@default:~/GIT/Day_4$ git log --oneline
e704400 (HEAD -> master) Revert "buggy commit"
c34adb4 buggy commit
c86f7d1 one more line of good code
</pre>
<p>In this example:</p>
<ul>
    <li>We initialized a Git repository and made two commits.</li>
    <li>We used <code>git revert c34adb4</code> to create a new commit that undoes the changes from the "buggy commit" while keeping the original commit history intact.</li>
    <li>The commit log shows the new revert commit at the top, preserving the previous commits.</li>
</ul>
