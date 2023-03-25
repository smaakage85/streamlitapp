# Instructions

Build container image:

```bash
. .env && \
podman build --build-arg python_version=${python_version} --no-cache -t ${app_name}:${branch} -f Dockerfile_streamlit
```

Run container on specific port:

```bash
. .env && \
podman run --rm -d -e FISK -p ${port}:8080 ${app_name}:${branch}
```
