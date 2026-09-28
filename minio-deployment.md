# MinIO Deployment

**Name:** CCM Jaymark Alqueza

## Deployment command

Run this command in the KillerCoda Ubuntu Playground:

```bash
docker run -d -p 9000:9000 -p 9001:9001 --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  minio/minio server /data --console-address ":9001"
```

The `-e` flags set environment variables inside the container. `MINIO_ROOT_USER` and `MINIO_ROOT_PASSWORD` configure the MinIO root login credentials used to access and administer the server.

## Ports

- **9000:** MinIO S3-compatible API.
- **9001:** MinIO Web Console. Use port **9001** in KillerCoda's port-access interface.

## Bucket and test object

- **Bucket:** `client-photos`
- **Uploaded object:** Record the filename of the safe sample image or text file uploaded to the bucket.

## Verification and evidence

After starting the container, verify it is running with:

```bash
docker ps --filter name=minio-server
```

Sign in to the console using the configured credentials, create the `client-photos` bucket, and upload a test object. Capture the terminal and bucket/object views and save the original screenshots as `screenshots/minio-deployed.png` and `screenshots/minio-bucket-upload.png`.

**Evidence status:** The KillerCoda deployment and screenshots have not been performed in this workspace. Add the actual screenshots and record the uploaded filename after completing those steps.

> The credentials above are provided for this lab only. Do not reuse them outside the disposable playground; production deployments should use unique secrets managed securely and should not expose the root account for routine access.
