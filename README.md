# hadoop-pseudodistributed
Easily install and setup hadoop single node cluster using vagrant.
Hadoop daemons run on the local machine, thus simulating a cluster on a small scale.
## Running
Go to cloned directory and run `vagrant up`. It will download the necessary artifacts and starts the virtual machine. To take shell to running virtual machine run `vagran ssh`

## WEB UI
Daemon | URL
--- | ---
Namenode | http://192.168.2.11:50070/
Resource manager |  http://192.168.2.11:8088/
History Server |  http://192.168.2.11:19888/
## Debug
* Status of the daemons can be found by running `jps`
* Logs of the Hadoop can be found at `/home/ubuntu/hadoop-2.7.3/logs`

## Prerequisites
Please have following components installed on the host system.

* Vagrant 1.9.1
* Virtualbox 5.1.14


