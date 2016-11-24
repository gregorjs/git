# Ceph @ UIBK


##Einige Fakten:

* Einsatz seit 2014 <!-- .element class="fragment" -->
* RBD produktiv seit 2015 <!-- .element class="fragment" -->
* RADOSGW seit 2015/16 <!-- .element class="fragment" -->
* Vanilla Variante <!-- .element class="fragment" -->


## Warum Vanilla?

* kein Vendor-lockin

* kein Hardware lockin

* weniger Gesamtkosten

* Transparenz

* Lernkurve für unified storage


## 2 Ceph Cluster
* Ceph Produktiv Cluster
  * 3 Mons, 4 Osd Nodes, Hammer
  * SSD journals
* Ceph Backup Cluster
  * 3 Mons, 2 Osd Nodes, Jewel
  * SSD journals


Anbindung über 
### Storage VLAN
### Storage Backend über VLAN


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
## Installationen!


## Installationsarten:

* Puppet (am Anfang)
* [Ansible](https://github.com/ceph/ceph-ansible)
* [Docker?](https://github.com/ceph/ceph-docker/tree/master/examples/kubernetes)


## positive Erfahrungen:

* sehr stabil <!-- .element class="fragment" -->
* läuft ohne Unterbruch <!-- .element class="fragment" -->
* Rolling Upgrades (manuell) <!-- .element class="fragment" -->
* ansible_ceph beste Codequalität <!-- .element class="fragment" -->


## weniger positive Erfahrungen:

* RPM Dependency Hell in Hammer <!-- .element class="fragment" -->
* RBD Kernelmodul <!-- .element class="fragment" -->
* richtigen Controller wählen! <!-- .element class="fragment" -->


## Performance
mit 
### caching
sehr gut


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