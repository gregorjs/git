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

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


## Everyday git

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

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


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

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


## Die Staging Area

![services](images/areas.png)


## Git Workflow

![services](images/lifecycle.png)


## git commit

<pre><code class="bash">git commit -m "Commit Message"
git commit -m "Inital Commit"
</code></pre>

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


## den letzten Commit rückgängig machen

<pre><code class="bash">git commit --amend
</code></pre>

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


## die Working Area und Staging Area zurücksetzen

<pre><code class="bash">git reset --hard
</code></pre>

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


## nur die Staging Area zurücksetzen

<pre><code class="bash">git reset --soft
</code></pre>

<iframe src="http://13.228.103.199:4200" style="
    background-color: white;
    height: 200px;
    width: 100%
"></iframe>


Vorteil:
### flexibler
als andere Virtualisierungen


Nachteil:
immer noch viele
### Entwicklungen
