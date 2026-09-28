# Cloud Storage Types

| Storage type | Description | Primary use case | Cloud provider example |
|---|---|---|---|
| Block Storage | Stores data in fixed-size blocks that a server can address and manage as a disk volume. | Boot volumes, databases, and workloads that need low-latency random access. | Amazon Elastic Block Store (Amazon EBS) |
| File Storage | Stores data as files in a hierarchy of directories, commonly accessed through shared file protocols. | Shared files, home directories, and applications that expect a network file system. | Amazon Elastic File System (Amazon EFS) |
| Object Storage | Stores each object (data, metadata, and a unique key) in a flat namespace, accessed through an API. | Large amounts of unstructured data such as photos, videos, backups, and logs. | Amazon Simple Storage Service (Amazon S3) |

**Recommendation to the client:** Object storage is a strong fit for user-uploaded images because it is designed to store large volumes of unstructured data and provides scalable access through APIs. Images can be stored independently from application containers, with metadata and unique keys that make objects straightforward to manage and retrieve.
