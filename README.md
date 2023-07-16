# 🚀 High Availability PostgreSQL

This is my simple Kubernetes configuration to deploy PostgreSQL with High Availability. This is the architecture looks like:

![PostgreSQL HA Architecture](./PostgreSQL%20HA%20Architecture.png)

I'm using StatefulSet to deploy the PostgreSQL container. Because a database is a stateful application that needs persistent data. I also use ConfigMap for PostgreSQL environment but you can use Secret as well. The cluster using two PersistentVolume as their volume. The PersistentVolumes using local-storage as their StorageClass and the StorageClass is on the local path. The Service is using NodePort to expose PostgreSQL port from outside also from inside.

### Made by Myself 🩵