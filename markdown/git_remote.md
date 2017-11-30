## Git Remotes


![Remotes](images/fcGAb.png)


## Remotes anzeigen

<pre><code class="bash">#Liste der remotes
git remote -v
</code></pre>

<pre><code class="bash lp">origin	git@github.com-gregorjs:gregorjs/git.git (fetch)
origin	git@github.com-gregorjs:gregorjs/git.git (push)
</code></pre>


## Remote hinzufügen

<pre><code class="bash">#Remote hinzufügen
git remote add remote_name remote_adresse
</code></pre>


## Klonen (Forken)

<pre><code class="bash">#clone
git clone git://remote_adresse
git clone https://remote_adresse
</code></pre>


## Push und Pull

<pre><code class="bash">#git push
git push remotename branchname
git push remotename lokaler_branch:remote_branch
#git poll
git pull remotename branchname
git pull remotename remote_branch:lokaler_branch
</code></pre>


## Push und Pull

![push und pull](images/UvZ0M.png)
