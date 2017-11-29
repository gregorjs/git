# GIT

Fast version control

* * *

Gregor Schwab | [`gregor.schwab@voestalpine.com`](mailto:gregor.schwab@voestalpine.com)

Git presentation @ Voestalpine | 29.11.2017


## Versionskontrollsysteme

* einfache Versionskontrolle <!-- .element class="fragment" -->
  * final, final2, really_final, ...<!-- .element class="fragment" -->
  * v1, v1.2.5,....<!-- .element class="fragment" -->
  * RCS, lokal <!-- .element class="fragment" -->

* Client - Server <!-- .element class="fragment" -->
  * CVS, SVN <!-- .element class="fragment" -->

* Distributed <!-- .element class="fragment" -->
  * GIT, Mercurial, Bazaar <!-- .element class="fragment" -->


## Kurze Entstehungsgeschichte von GIT

* 2006 von Linus Torvalds entwickelt
* Schwerpunkt Softwareentwicklung (Linux Kernel)
* Unzufriedenheit mit bestehenden Systemen


## Vorteile von GIT

* schneller
* kein Server nötig (Committen, Mergen, branchen wann immer man will)
* einfachere Kollaboration durch Pull Requests, Forks,

   Soziale Netzwerke (Github,...)


## DVCS vs. VCS

* Snapshots (keine Deltas)
* Lightweight Forks, wie DNA
* Keine Network Latency
* Sauberes Merge Tracking
* Datenintegrität ([SHA1](https://en.wikipedia.org/wiki/SHA-1) Summen)
* Meritocracy anstelle Comitter Status
* Lokale Branches (ermöglicht privates Arbeiten und neue Ideen)


## Installation von GIT

https://git-scm.com/downloads

* Unter Windows:
https://git-scm.com/download/win

* Unter Linux (z.B. über Packagemanager):
<pre><code class="bash"># Installation von git auf Ubuntu
  $ apt-get install git-all
</code></pre>

* Selbst kompilieren (nicht empfohlen)


## Warum Ceph

* distributed <!-- .element class="fragment" -->

* scalable <!-- .element class="fragment" -->

* free as in speech <!-- .element class="fragment" -->


## Warum nicht Ceph?

* Performance <!-- .element class="fragment" -->

* Stabilität <!-- .element class="fragment" -->

* Benutzerfreundlichkeit <!-- .element class="fragment" -->


Kann Ceph produktiv eingesetzt werden?

Dies hängt von der Betrachtung ab
### RADOS object store, RBD, und RadosGW
gelten als ausreichend stabil
grosse Organisationen verwenden es
### CephFS is stabil seit Jewel
(ohne Snapshots)

tendentiell stabiler als so manch kommerzielles
System


## Ceph Release Cycle

![release](images/release.png)


## Ceph Developer Community

![developers](images/developers.png)


## Ceph besteht aus

* OSDs

* Monitors

* MDS

![services](images/services.png)


Ceph ist eigentlich ein
# Object Store

![objectstore](images/objectstore.png)


## Was ist Ceph nicht?


# Ceph ≠ RAID


## Ceph beherrscht aber
* Striping
* Replicas
* Erasure Coding
* Cache Pools


Ceph bietet mehrere
## Storage Frontends


* RBD
* RADOS Gateway
* CephFS


<!-- .slide: data-background-image="images/stack.png" data-background-size="contain" -->


## RBD
über
## qemu-librbd
(caching)


#Ceph und Hyperconverged?


<!-- .slide: data-background-image="images/hci-in-depth.png" data-background-size="contain" -->


Unterstützung für
#Ceph
in
#Openstack?


<!-- .slide: data-background-image="images/openstack-ceph-galaxy.png" data-background-size="contain" -->


Unterstützung für
#Ceph
in
#RHEV?

* seit RHEV 3.6
