# GIT

Fast version control

* * *

Gregor Schwab | [`gregor.schwab@voestalpine.com`](mailto:gregor.schwab@voestalpine.com)

Git presentation @ Voestalpine | 30.11.2017


## Zu meiner Person

* Studium an der Universität Innsbruck
* 1994+ versch. Softwareentwicklung mit C++, Java (JBoss) und Perl (Philips)
* 1994+ Erstkontakt mit Unix Workstations und RCS
* 2004+ techn. Infrastruktur Standortleitung Sysadmins
* 2011+ Leitung der Webentwicklung (EA Startup Turbulenz)


* 2013+ Teamleitung Virtualisierungsinfrastruktur am ZID (Universität Innsbruck)
  für 4000 Mitarbeiter und ca. 40.000 Studierende
  Planung, Betreuung und Weiterentwicklung des Gitlab Community Edition Servers der Universität Innsbruck (800 Benutzer über 1000 Projekte)
  Entwicklung der Puppet Deployment Infrastruktur mit Tests/CI/CD
* 2015+ SCRUM Master Ausbildung
* 2015+ Projektmanagement div. DevOPS Projekte


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
  $ apt-get install git
</code></pre>

* Selbst kompilieren (nicht empfohlen)


## Installation unter Windows im Detail

![setup1](images/Setup1.png)


## Installation unter Windows im Detail

![setup2](images/Setup2.png)


## Installation unter Windows im Detail

![setup3](images/Setup3.png)


## Installation unter Windows im Detail

![setup4](images/Setup4.png)


## Installation der SSH Keys (optional)

<pre><code class="bash">ssh-keygen -t rsa -C "your_email@example.com"
</code></pre>

![setup5](images/Setup5.png)
