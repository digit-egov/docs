# Cluster Requirements

### Requirements <a id="requirements"></a>

#### Master Cluster <a id="master-cluster"></a>

* Six or more machines running one of:
  * Ubuntu 16.04+
  * Debian 9
  * CentOS 7
  * RHEL 7
  * Container Linux \(tested with 1576.4.0\)
* 4 GB or more of RAM per machine \(any less will leave little room for your apps\)
* 2 CPUs or more

#### User Cluster <a id="user-cluster"></a>

* One or more machines running one of:
  * Ubuntu 16.04+
  * Debian 9
  * CentOS 7
  * RHEL 7
  * Container Linux \(tested with 1576.4.0\)
* 2 GB or more of RAM per machine \(any less will leave little room for your apps\)
* 2 CPUs or more
* Full network connectivity between all machines in the cluster \(public or private network is fine\)
* Unique hostname, MAC address, and product\_uuid for every node. See [here](cluster-requirements.md#verify-the-mac-address-and-product-uuid-are-unique-for-every-node) for more details.
* Certain ports are open on your machines. See below for more details.
* Swap disabled. You **MUST** disable swap in order for the kubelet to work properly.

#### Verify the MAC Address and `product_uuid` Are Unique for Every Node <a id="verify-the-mac-address-and-product_uuid-are-unique-for-every-node"></a>

* You can get the MAC address of the network interfaces using the command `ip link` or `ifconfig -a`
* The product\_uuid can be checked by using the command `sudo cat /sys/class/dmi/id/product_uuid`

It is very likely that hardware devices will have unique addresses, although some virtual machines may have identical values. Kubernetes uses these values to uniquely identify the nodes in the cluster. If these values are not unique to each node, the installation process may [fail](https://github.com/kubernetes/kubeadm/issues/31).

#### Check Network Adapters <a id="check-network-adapters"></a>

If you have more than one network adapter, and your Kubernetes components are not reachable on the default route, we recommend you add IP route\(s\) so Kubernetes cluster addresses go via the appropriate adapter.

#### Check Required Ports <a id="check-required-ports"></a>

**Master Cluster Master Node\(s\)**

| Protocol | Direction | Port Range | Purpose |
| :--- | :--- | :--- | :--- |
| TCP | Inbound | 6443\* | Kubernetes API server |
| TCP | Inbound | 2379-2380 | etcd server client API |
| TCP | Inbound | 10250 | kubelet API |
| TCP | Inbound | 10251 | kube-scheduler |
| TCP | Inbound | 10252 | kube-controller-manager |
| TCP | Inbound | 10255 | Read-only kubelet API |

**Worker Node\(s\)& User Cluster Worker Nodes**

| Protocol | Direction | Port Range | Purpose |
| :--- | :--- | :--- | :--- |
| TCP | Inbound | 10250 | kubelet API |
| TCP | Inbound | 10255 | Read-only kubelet API |
| TCP | Inbound | 30000-32767 | NodePort Services\*\* |

\*\* Default port range for [NodePort Services](https://kubernetes.io/docs/concepts/services-networking/service/).

Any port numbers marked with \* are overridable, so you will need to ensure any custom ports you provide are also open.

