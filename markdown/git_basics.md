# Git Setup

Erstmalig:

<pre><code class="bash"># Benutzerparameter für GIT
  git config --global user.name "Your Name"
  git config --global user.email "your_email@whatever.com"
</code></pre>

* /etc/gitconfig (global) <!-- .element class="fragment" -->
* ~/.gitconfig oder %USERPROFILE%/.gitconfig (benutzerspezifisch) <!-- .element class="fragment" -->
* PROJEKTORDNER/.git/config (projektspezifisch) <!-- .element class="fragment" -->

<pre><code class="bash"># GIT Einstellungen abfragen
git config --list
</code></pre>


## Das GIT Repository

* Das .git Verzeichnis <!-- .element class="fragment" -->
* Die Working Area (checkout) <!-- .element class="fragment" -->
* Die Staging Area <!-- .element class="fragment" -->


## Everyday git

<pre><code class="bash">git init
</code></pre>


## Git status

<pre><code class="bash">#Status abfragen
git status
</code></pre>

<pre><code class="bash lp">git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	hello.js

nothing added to commit but untracked files present (use "git add" to track)
</code></pre>


## Dateien in der Staging Area ignorieren

.gitignore


## git add (Staging)

<pre><code class="bash">git add file
git add \*.c
git add .
</code></pre>

<pre><code class="bash lp"> git add hello.js
gregor@ip-172-31-16-42:~/test$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   hello.js
</code></pre>


## Die Staging Area (der Index)

![staging area](images/areas.png)


## Git Workflow

![git workflow](images/lifecycle.png)


## git commit

<pre><code class="bash">git commit -m "Commit Message"
git commit -m "Inital Commit"
</code></pre>

<pre><code class="bash lp">[master d4b7ff2] Inital Commit
 1 file changed, 1 insertion(+), 1 deletion(-)
</code></pre>


## den letzten Commit rückgängig machen

<pre><code class="bash">git commit --amend
</code></pre>

<pre><code class="bash lp">git commit --amend
Inital Commit

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# Author:    Gregor <gregor@ip-172-31-16-42.ap-southeast-1.compute.internal>
# Date:      Wed Nov 29 22:30:55 2017 +0000
#
# On branch master
#
# Initial commit
#
# Changes to be committed:
#       new file:   hello.js
#
</code></pre>


## die Working Area und Staging Area zurücksetzen

<pre><code class="bash">git reset --hard
#nur das Ändern einer Datei in der Working Area rückgängig machen
git checkout -- CONTRIBUTING.md
</code></pre>


## nur die Staging Area zurücksetzen (Unstage)

<pre><code class="bash">git reset
git reset DATEINAME
</code></pre>


## Dateien löschen

<pre><code class="bash">#Datei entfernen
rm hello.js
#Die Datei aus der Staging Area löschen
git rm hello.js
git rm --cached hello.js #Datei behalten
</code></pre>

<pre><code class="bash lp">git rm hello.js
HEAD detached at v1
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	deleted:    hello.js
</code></pre>


## Dateien umbenennen

<pre><code class="bash">#Datei umbennenen
git mv hello.js hallo.js

mv hello.js hallo.js
git add hallo.js
git rm hello.js
</code></pre>

<pre><code class="bash lp">git status
HEAD detached at v1
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	deleted:    hello.js

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	hallo.js

no changes added to commit (use "git add" and/or "git commit -a")
</code></pre>


## git diff

<pre><code class="bash">#Die Differenz der Working Area zum letzten Commit
git diff
#Die Differenz der Staging Area zum letzten Commit
git diff --staged
</code></pre>

<pre><code class="bash lp">git diff
diff --git a/hello.js b/hello.js
index 8a00f7c..481e5ca 100644
--- a/hello.js
+++ b/hello.js
@@ -1 +1 @@
-console.log ("Hello World!")
+console.log ("Hallo Welt!")
</code></pre>


## Tagging

<pre><code class="bash">#dem momentanen HEAD den TAG v1 geben
git tag v1
git tag v1 CommitNo
git checkout v1^
git tag v1-beta
</code></pre>

<pre><code class="bash">#Tags ansehen
git tag
</code></pre>


## History

<pre><code class="bash">#die letzten Commits anzeigen
git log
git log --since=yesterday
#Übersichtlichere Darstellung
git log --pretty=format:"%h %ad | %s%d [%an]"
--graph --date=short
</code></pre>

<pre><code class="bash">#ein Alias in .gitconfig definieren
[alias]
  hist = log --pretty=format:\"%h %ad | %s%d [%an]\" --graph --date=short
</code></pre>

<pre><code class="bash lp">git hist
d4b7ff2 Wed Nov 29 23:24:14 2017 +0000 | Inital Commit (HEAD -> master, tag: v1) [Gregor Schwab]
6d3c67a Wed Nov 29 22:30:55 2017 +0000 | Second Commit [Gregor]
</code></pre>


## Branches

<pre><code class="bash">#einen neuen lokalen Branch anlegen
git branch name
git branch
git branch -a #zeigt auch remote branches
</code></pre>

<pre><code class="bash lp">git branch
  feature
* master
</code></pre>

<pre><code class="bash">#einen neuen lokalen Branch anlegen
git checkout branch #(-b) legt neuen branch an
</code></pre>

<pre><code class="bash lp">git checkout feature
Switched to branch 'feature'
</code></pre>


## Der master branch

![master branch](images/branch-and-history.png)


## create new branch

![basic branches](images/head-to-master.png)


## switch to new branch

![checkout master](images/head-to-testing.png)


## checkout master again

![checkout master](images/checkout-master.png)


## advance master

![advance master](images/advance-master.png)


## Branches

![topic branches](images/topic-branches-1.png)


## Merging

<pre><code class="bash">#einen Branch in einen anderen mergen
git merge branch1 branch2
git merge branch #den branch in den momentanen checkout mergen
</code></pre>

<pre><code class="bash lp">git branch
  feature
* master
</code></pre>


## Basic Merging

![basic merging](images/basic-merging-2.png)
