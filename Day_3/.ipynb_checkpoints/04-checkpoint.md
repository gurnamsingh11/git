<h1>Git Diff</h1>

<h2>Understanding Git Diff Syntax</h2>
<p>The <code>git diff</code> command shows the differences between files or commits. Here’s the basic syntax for the diff output:</p>
<pre>
diff --git a/my_file.txt b/my_file.txt
index a163a61..622f819 100644
--- a/my_file.txt
+++ b/my_file.txt
@@ -1,3 +1,4 @@
 ONE LINE
 TWO LINE
-THREE LINE
\ No newline at end of file
+THREE LINE
+For
\ No newline at end of file
</pre>

<p>In the diff output:</p>
<ul>
  <li><code>a</code> and <code>b</code> represent the versions being compared.</li>
  <li><code>---</code> denotes the old version (committed version).</li>
  <li><code>+++</code> denotes the new version (updated version).</li>
  <li>The lines beginning with <code>-</code> are removed from the old version.</li>
  <li>The lines beginning with <code>+</code> are added in the new version.</li>
  <li>Lines not prefixed by <code>-</code> or <code>+</code> show unchanged context.</li>
</ul>

<p>Learn more at <a href="https://git-scm.com/docs/git-diff">Git Diff Documentation</a>.</p>

<h2>Example Outputs</h2>
<pre>
sagemaker-user@default:~/GIT/Day_3$ git add my_file.txt 

sagemaker-user@default:~/GIT/Day_3$ git diff
diff --git a/my_file.txt b/my_file.txt
index a163a61..622f819 100644
--- a/my_file.txt
+++ b/my_file.txt
@@ -1,3 +1,4 @@
 ONE LINE
 TWO LINE
-THREE LINE
\ No newline at end of file
+THREE LINE
+For
\ No newline at end of file
</pre>

<pre>
sagemaker-user@default:~/GIT/Day_3$ git diff
diff --git a/my_file.txt b/my_file.txt
index a163a61..e1f83a7 100644
--- a/my_file.txt
+++ b/my_file.txt
@@ -1,3 +1,4 @@
 ONE LINE
 TWO LINE
-THREE LINE
\ No newline at end of file
+NEW LINE
+UNCOMMITED NEW THREE LINE
</pre>

<pre>
sagemaker-user@default:~/GIT/Day_3$ git diff
diff --git a/master.txt b/master.txt
index f381643..1255340 100644
--- a/master.txt
+++ b/master.txt
@@ -1 +1,2 @@
-continued development in master
\ No newline at end of file
+continued development in master
+add a new line to master text file
\ No newline at end of file
diff --git a/my_file.txt b/my_file.txt
index a163a61..e1f83a7 100644
--- a/my_file.txt
+++ b/my_file.txt
@@ -1,3 +1,4 @@
 ONE LINE
 TWO LINE
-THREE LINE
\ No newline at end of file
+NEW LINE
+UNCOMMITED NEW THREE LINE
</pre>
