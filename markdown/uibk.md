# Ceph @ UIBK

<img src="images/ceph_logo.png" style="width:20%"/>


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