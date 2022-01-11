- Documented Dockerfile example:

```dockerfile
# Define base image
FROM alpine

# Install additional dependencies
RUN apk add --update redis

# Define what to do when the container starts
CMD ["redis-server"]

```

- Build command:
```bash
docker build . 
```