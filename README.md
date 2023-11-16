# Build Image

```bash
docker build -t myapp:v1 .
```

# Run Container removing after stop

```bash
docker run --name myapp_nodemon -p 4000:4000 --rm myapp:v1
```

# Run Container with volume removing after stop

```bash
docker run --name myapp_nodemon -p 4000:4000 -v $(pwd):/app -v /app/node_modules --rm myapp:v1
```

# Run Container keeping after stop

```bash
docker run --name myapp_nodemon -p 4000:4000 myapp:v1
```

# Run Container detached keeping after stop

```bash
docker run -d --name myapp_nodemon -p 4000:4000 myapp:v1
```

# Stop Container

```bash
docker stop myapp_nodemon
```