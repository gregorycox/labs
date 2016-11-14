# Exploring Kubernetes with libStorage persistent volumes on AWS - the Hard Way

Persistent volumes are intended for "network volumes" like GCE persistent disks, and AWS elastic block stores, but can also represent volumes from "overlay" storage providers like ScaleIO. A Persistent Volume (PV) in Kubernetes represents a real piece of underlying storage capacity in the infrastructure. 

A user (application) sees and consumes claims, which hide storage implementation details. This allows an application's configuration to be portable across platforms and providers.

Dynamic provisioning is a mechanism that allows storage volumes to be created on demand, rather than pre-provisioned by an administrator. This is a Beta feature of Kubernetes 1.4.

Create a storage class: