<h1>Undergoing Changes</h1>

<h2>Git Checkout and Detached Head</h2>
<p>The <code>git checkout</code> command is used to switch between different versions of files, commits, and branches. It allows you to explore historical commits without undoing any previous work.</p>
<p>For example, to switch to a different branch, you can use:</p>
<pre>
git checkout branch_name
</pre>
<p>Alternatively, you can use <code>git switch branch_name</code> for branch switching, but <code>git checkout</code> can also operate on commits:</p>
<pre>
git log --oneline
git checkout ####### (first seven characters of the commit hash)
</pre>
<p>This command checks out the specified commit without altering your working directory or undoing any previous work.</p>

<h2>Git Restore</h2>
<p>The <code>git restore</code> command is used to restore working directory files to a previous state or undo changes in the working directory or index (staging area). For instance:</p>
<pre>
git restore <file>      # Restore file to its last committed state
git restore --source=HEAD --staged <file>  # Unstage file
</pre>

<h2>Git Reset</h2>
<p>The <code>git reset</code> command is used to reset your index and working directory to a specified state. This command can be used to undo commits and changes in various ways:</p>
<ul>
  <li><code>git reset --soft <commit></code> - Resets the index but keeps changes in the working directory.</li>
  <li><code>git reset --mixed <commit></code> - Resets the index and updates the working directory, but does not remove changes.</li>
  <li><code>git reset --hard <commit></code> - Resets the index and working directory to the specified commit, discarding all changes.</li>
</ul>

<h2>Git Revert</h2>
<p>The <code>git revert</code> command is used to create a new commit that undoes the changes made by a previous commit. This is useful for undoing changes in a way that preserves the commit history:</p>
<pre>
git revert <commit>
</pre>
<p>This command generates a new commit that reverses the changes introduced by the specified commit.</p>
