# Kubernetes Volume and Storage Commands

This document provides an overview of Kubernetes volume and storage-related commands.

# Volume Management Commands

## Create a PersistentVolume (PV)
To create a PersistentVolume (PV) object, use the following command:
`kubectl create -f <pv-definition.yaml>`

## Create a PersistentVolumeClaim (PVC)
To create a PersistentVolumeClaim (PVC) object, use the following command:
`kubectl create -f <pvc-definition.yaml>`

## List PersistentVolumes
To list all PersistentVolumes in the cluster, use the following command:
`kubectl get pv`

## List PersistentVolumeClaims
To list all PersistentVolumeClaims in the cluster, use the following command:
`kubectl get pvc`

## Describe a PersistentVolume
To get detailed information about a specific PersistentVolume, use the following command:
`kubectl describe pv <pv-name>`

## Describe a PersistentVolumeClaim
To get detailed information about a specific PersistentVolumeClaim, use the following command:
`kubectl describe pvc <pvc-name>`

## Delete a PersistentVolume
To delete a PersistentVolume, use the following command:
`kubectl delete pv <pv-name>`

## Delete a PersistentVolumeClaim
To delete a PersistentVolumeClaim, use the following command:
`kubectl delete pvc <pvc-name>`

# StorageClass Management Commands

## Create a StorageClass
To create a StorageClass, use the following command:
`kubectl create -f <storage-class-definition.yaml>`

## List StorageClasses
To list all StorageClasses in the cluster, use the following command:
`kubectl get sc`

## Describe a StorageClass
To get detailed information about a specific StorageClass, use the following command:
`kubectl describe sc <storage-class-name>`

## Delete a StorageClass
To delete a StorageClass, use the following command:
`kubectl delete sc <storage-class-name>`

# Dynamic Provisioning Commands

## Enable Dynamic Provisioning
To enable dynamic provisioning using a StorageClass, ensure that the StorageClass is created and marked as the default StorageClass. For example, if you have a StorageClass named "standard" and you want to mark it as default, use the following command:
`kubectl patch storageclass standard -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'`

## Create a PVC with Dynamic Provisioning
To create a PersistentVolumeClaim with dynamic provisioning, use the following command:
`kubectl create -f <pvc-definition.yaml>`

# Volume Snapshot Commands

## Create a VolumeSnapshot
To create a VolumeSnapshot, use the following command:
`kubectl create -f <volume-snapshot-definition.yaml>`

## List VolumeSnapshots
To list all VolumeSnapshots in the cluster, use the following command:
`kubectl get volumesnapshot`

## Describe a VolumeSnapshot
To get detailed information about a specific VolumeSnapshot, use the following command:
`kubectl describe volumesnapshot <volumesnapshot-name>`

## Delete a VolumeSnapshot
To delete a VolumeSnapshot, use the following command:
`kubectl delete volumesnapshot <volumesnapshot-name>`
