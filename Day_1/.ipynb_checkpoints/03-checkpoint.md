<h1>How to create a Git Repository?</h1>

<h2>git init</h2>
<p>This command initializes a Git Repository on your local machine.</p>
<p>You only need to run this command once per project.</p>

<h2>git status</h2>
<p>This command will report back the status of your Git repository.</p>

<p>Using <code>git init</code> we will create a hidden git file that will hold all the information. All the changes are tracked.</p>

<h2>Example Commands</h2>
<p><code>sagemaker-user@default:~/GIT$ git init</code></p>
<p>Initialized empty Git repository in /home/sagemaker-user/GIT/.git/</p>

<p><code>sagemaker-user@default:~/GIT$ git status</code></p>
<p>On branch master</p>
<p>No commits yet</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<p><code>sagemaker-user@default:~/GIT$ git status</code></p>
<p>On branch master</p>
<p>No commits yet</p>
<p>nothing added to commit but untracked files present (use "git add" to track)</p>

<p><code>sagemaker-user@default:~/GIT$ git clone https://github.com/gurnamsingh11/git-course.git</code></p>
<p>Cloning into 'git-course'...</p>

<p><code>sagemaker-user@default:~/GIT$ cd git-course/</code></p>

<p><code>sagemaker-user@default:~/GIT/git-course$ dir</code></p>
<p>README.md</p>

<h1>Cloning Private Repos:</h1>

<h2>Option 1: Command Line</h2>
<p>Create Personal Access Tokens (PAT) on Github.com</p>
<p>When using the <code>git clone</code> command, reference the PAT</p>

<h2>Option 2: Github Desktop Tool GUI</h2>
<p>Open the Github Desktop Tool</p>
<p>Login with Github Username and PW</p>
<p>Clone Repo via GUI</p>

<h2>Clone Syntax with PAT</h2>
<p><code>git clone https://token@github.com/account/repo.git</code></p>
