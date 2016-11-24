### RadosGW über 2 HAProxys


![Ceph_RGW_Haproxy](images/Ceph_RGW_Haproxy.svg)


##  RBD 
über 
## Cinder 
in 
* Openstack
* RHEV


![rhev1](images/cinder.png)


![rhev2](images/pools.png)


## RBD Backups
über
## [Incremental Snapshots](http://ceph.com/dev-notes/incremental-snapshots-with-rbd/)


## RADOS Backups
über 
## RGW Multisite
(noch s3sync, 
ersetzt federated gateways) 


# Installation:


keine 
## manuellen
Installationen
## Automatisieren!


<video class="stretch" data-autoplay src="videos/tom.mp4"></video>


## Installationsarten:

* Puppet (am Anfang)
* [Ansible](https://github.com/ceph/ceph-ansible)
* [Docker?](https://github.com/ceph/ceph-docker/tree/master/examples/kubernetes)


## positive Erfahrungen:

* sehr stabil <!-- .element class="fragment" -->
* läuft ohne Unterbruch <!-- .element class="fragment" -->
* Rolling Upgrades (manuell) <!-- .element class="fragment" -->
* ansible_ceph beste Codequalität <!-- .element class="fragment" -->


## weniger schöne Erfahrungen:

* RPM Dependency Hell in Hammer <!-- .element class="fragment" -->
* RBD Kernelmodul <!-- .element class="fragment" -->
* richtigen Controller wählen! <!-- .element class="fragment" -->
* [parted-3.2" package BUG](http://tracker.ceph.com/issues/15918) <!-- .element class="fragment" -->


## Performance
mit 
### caching
sehr gut


## Operations:


Auskonfigurieren einer kaputten OSD

<pre><code data-trim data-noescape>
out.sh
#!/bin/bash
ceph osd out $1
sudo service ceph-osd@$1 stop
ceph osd crush remove osd.$1
ceph auth del osd.$1
ceph osd rm $1
sudo umount /var/lib/ceph/osd/ceph-$1
sudo rmdir /var/lib/ceph/osd/ceph-$1
</code></pre>


Einhängen einer neuen OSD

<pre><code data-trim data-noescape>
#!/bin/bash
CLUSTER_UUID="YOUR UUID"
disk=/dev/sdx
journal=/dev/sda2
ceph-disk prepare --cluster ceph --cluster-uuid $CLUSTER_UUID --fs-type xfs ${disk} ${journal}
ceph-disk activate ${disk}
</code></pre>


## Ausblick:

* Hybrid Cluster (SSD, HDD) <!-- .element class="fragment" -->
* Ceph on Flash <!-- .element class="fragment" -->
* Bluestore (Kraken Release) <!-- .element class="fragment" -->
* DPDK Stack (Kraken Release) <!-- .element class="fragment" -->
* Erasure code overwrites, append only (Kraken Release) <!-- .element class="fragment" -->
* ceph-mgr for metrics <!-- .element class="fragment" -->
* RBD ordered writeback cache, low latency <!-- .element class="fragment" -->


![ceph_on_flash](images/ceph_on_flash.png)


### Ordered writeback cache


![wb0](images/wb0.png)


![wb1](images/wb1.png)


![wb2](images/wb2.png)