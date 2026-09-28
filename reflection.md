# Mission Reflection

**Name:** CCM Jaymark Alqueza

Object storage is better suited to millions of photos than a traditional block-storage hard drive because it is built to keep large amounts of unstructured data as independent objects, each with a unique key and metadata. A block volume behaves more like a disk attached to a server: the application or operating system must organize and manage its contents. Object storage can scale to very large collections and lets applications retrieve images through an API, without tying those files to the lifetime or capacity of one web-server container.

Docker makes deploying MinIO easier because the server and its runtime are packaged together in a container image. A single command can start the service, map the API and console ports, and provide configuration through environment variables. This avoids manually installing and configuring the storage server on the playground host and makes the setup easier to reproduce. The container still needs durable storage configured for data that must survive its removal; a container by itself is not a backup.

A bucket is a named container for objects in an object-storage service. It provides an organizational and administrative boundary in which an application can store and retrieve objects, such as uploaded photos.

Large enterprises reduce the risk of data loss by keeping redundant copies across drives, machines, and often separate availability zones or regions. They may use erasure coding, versioning, replication, integrity checks, monitoring, and tested backups. These measures help recover from individual hardware failures, accidental deletion, and larger outages, although the exact design depends on availability and recovery requirements.

Working through this lab helps me become more comfortable with the Linux command line. Docker commands make it clearer how flags, port mappings, and environment variables affect a service. I also see that command-line work is not only about starting a process: checking container status, validating access, and recording evidence are important parts of operating infrastructure. Completing the console steps in KillerCoda will give me practice connecting a running service to a browser and verifying the result.
