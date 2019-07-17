# Introducing available volume types

1. emptyDir —A simple empty directory used for storing transient data.

2. hostPath —Used for mounting directories from the worker node’s filesystem
   into the pod.
   
3. gitRepo —A volume initialized by checking out the contents of a Git repository.

4. nfs —An NFS share mounted into the pod.

5. gcePersistentDisk (Google Compute Engine Persistent Disk), awsElastic-
   BlockStore (Amazon Web Services Elastic Block Store Volume), azureDisk
   (Microsoft Azure Disk Volume)—Used for mounting cloud provider-specific
   storage.
   
6. cinder , cephfs , iscsi , flocker , glusterfs , quobyte , rbd , flexVolume , vsphere-
   Volume , photonPersistentDisk , scaleIO —Used for mounting other types of
   network storage.
   
7. configMap , secret , downwardAPI —Special types of volumes used to expose cer-
   tain Kubernetes resources and cluster information to the pod.
   
8. persistentVolumeClaim —A way to use a pre- or dynamically provisioned per-
   sistent storage. (We’ll talk about them in the last section of this chapter.)
   