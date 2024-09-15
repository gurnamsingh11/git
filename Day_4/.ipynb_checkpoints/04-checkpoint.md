<h1>Git Reset</h1>

<h2>Overview</h2>
<p>The <code>git reset</code> command allows you to remove commits and "reset" the branch to a specific state. There are two main types of <code>git reset</code> calls:</p>
<ul>
    <li><code>git reset <commit></code> - Removes commits in front of the specified commit hash, but keeps the changes in the working directory.</li>
    <li><code>git reset <commit> --hard</code> - Removes commits and discards changes in the working directory and staging area.</li>
</ul>

<h2>Use Cases</h2>
<p>Using <code>git reset</code> without the <code>--hard</code> flag will only affect the commit history, not the files themselves. This can be useful if you accidentally committed to the wrong branch. If you want to discard changes in the files as well, you should use the <code>--hard</code> flag.</p>

<h2>Examples</h2>
<p>Here’s an example workflow demonstrating how to use <code>git reset</code>:</p>
<pre>
sagemaker-user@default:~/GIT/Day_4$ git init
Initialized empty Git repository in /home/sagemaker-user/GIT/Day_4/.git/

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "one commit"
[master (root-commit) 12d3fc3] one commit
 1 file changed, 1 insertion(+)

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "two commit"
[master 0005c62] two commit
 1 file changed, 2 insertions(+), 1 deletion(-)

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "three commit"
[master bd1e13a] three commit
 1 file changed, 2 insertions(+), 1 deletion(-)

sagemaker-user@default:~/GIT/Day_4$ git log --oneline
bd1e13a (HEAD -> master) three commit
0005c62 two commit
12d3fc3 one commit

sagemaker-user@default:~/GIT/Day_4$ git reset 0005c62
Unstaged changes after reset:
M       myfile.txt

sagemaker-user@default:~/GIT/Day_4$ git log --oneline
0005c62 (HEAD -> master) two commit
12d3fc3 one commit

sagemaker-user@default:~/GIT/Day_4$ git add myfile.txt
sagemaker-user@default:~/GIT/Day_4$ git commit -m "updated commit"
[master abc948a] updated commit
 1 file changed, 2 insertions(+), 1 deletion(-)

sagemaker-user@default:~/GIT/Day_4$ git log --oneline
abc948a (HEAD -> master) updated commit
0005c62 two commit
12d3fc3 one commit

sagemaker-user@default:~/GIT/Day_4$ git reset 0005c62 --hard
HEAD is now at 0005c62 two commit
</pre>
<p>In this example:</p>
<ul>
    <li>We initialized a Git repository and made three commits.</li>
    <li>We used <code>git reset 0005c62</code> to remove commits after a specific commit but kept the changes in the working directory.</li>
    <li>We added and committed the changes, creating a new commit.</li>
    <li>We used <code>git reset 0005c62 --hard</code> to remove commits and discard changes in the working directory.</li>
</ul>
