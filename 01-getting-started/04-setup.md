# Set Up a Linux Environment on Windows and macOS

There are several ways to set up a Linux environment on Windows or macOS, including using `cloud VM`, `WSL2`, `VirtualBox`, `Hyperkit`, and more. However, I recommend using **Docker** to create a Linux container. This method is lightweight, cost-effective, and avoids connectivity issues.

## Step-by-Step Guide to Running an Ubuntu Container

1. **Install Docker Desktop**  
   Download and install Docker Desktop for your operating system from [here](https://www.docker.com/products/docker-desktop/).

2. **Run Ubuntu Linux Container**  
   Use the following command to run an Ubuntu container. It will be persistent and can be used long-term.

### Docker Command to Run Ubuntu Linux Container (Persistent & Long-Term)

```bash
docker run -dit \
  --name ubuntu-container \
  --hostname ubuntu-dev \
  --restart unless-stopped \
  --cpus="2" \
  --memory="4g" \
  --mount type=bind,source=C:/ubuntu-data,target=/data \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -p 2222:22 \
  -p 8080:80 \
  --env TZ=Asia/Kolkata \
  --env LANG=en_US.UTF-8 \
  ubuntu:latest /bin/bash

## Explanation of Parameters

| Parameter                                       | Description                                                                                     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------|
| `-dit`                                          | Runs the container in detached (-d), interactive (-i), and terminal (-t) mode.                   |
| `--name ubuntu-container`                       | Names the container for easier management.                                                      |
| `--hostname ubuntu-dev`                         | Sets the container's hostname to "ubuntu-dev".                                                   |
| `--restart unless-stopped`                      | Ensures the container restarts automatically unless stopped manually.                            |
| `--cpus="2"`                                    | Allocates 2 CPU cores to the container.                                                         |
| `--memory="4g"`                                 | Allocates 4GB of RAM to the container.                                                          |
| `--mount type=bind,source=C:/ubuntu-data,target=/data` | Mounts a folder from your local system into the container to persist data.                        |
| `-v /var/run/docker.sock:/var/run/docker.sock`  | Allows running Docker commands inside the container (optional).                                 |
| `-p 2222:22`                                    | Maps port 2222 on the host to port 22 (SSH) inside the container.                               |
| `-p 8080:80`                                    | Maps port 8080 on the host to port 80 (for web services) inside the container.                   |
| `--env TZ=Asia/Kolkata`                         | Sets the timezone (modify based on your location).                                               |
| `--env LANG=en_US.UTF-8`                        | Sets the language (modify if needed).                                                           |
| `ubuntu:latest /bin/bash`                       | Uses the latest Ubuntu image and starts the Bash shell.                                          |
