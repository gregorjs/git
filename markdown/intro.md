#Ceph 
an der
# Universität Innsbruck
[`gregor.schwab@uibk.ac.at`](mailto:gregor.schwab@uibk.ac.at)


## Was ist Ceph?


Ceph ist ein
## Software defined Storage (SDS)
System


Ceph wurde von
##[Sage Weil](https://en.wikipedia.org/wiki/Sage_Weil) 
in der Firma
## Inktank
entwickelt und 2014 von
## Redhat
gekauft


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

