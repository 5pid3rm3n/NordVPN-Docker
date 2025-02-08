# 🚀 NordVPN Docker

Welcome to the **NordVPN Docker** repository! This project provides a Dockerfile to create a Docker image with NordVPN installed. Secure your internet connection effortlessly with Docker and NordVPN.

📚 **NordVPN Docker build docs**:
[NordVPN Docs](https://support.nordvpn.com/hc/en-us/articles/20465811527057-How-to-build-the-NordVPN-Docker-image)

## 🛠️ Building the Docker Image

To build the Docker image locally, run the following command:

```sh
docker build -t your-dockerhub-username/nordvpn:latest .
```

## 🚢 Running the Docker Container

To run the Docker container, use the following command:

```sh
sudo docker run -it --hostname mycontainer --cap-add=NET_ADMIN --sysctl net.ipv6.conf.all.disable_ipv6=0 your-dockerhub-username/nordvpn:latest
```

### 🔍 Explanation:

- `-it`: Allocates a pseudo-TTY connected to the container’s stdin, creating an interactive bash shell in the container.
- `--cap-add`: Adds capabilities needed to successfully run the NordVPN Daemon and connect to NordVPN servers.
- `--sysctl net.ipv6.conf.all.disable_ipv6=0`: Disables IPv6 traffic on Linux for the NordVPN container, ensuring no leaks after connecting to NordVPN servers.
- `--hostname`: Sets the hostname for your container to prevent the Meshnet hostname from changing after restarting the Docker container.

## 📜 License

This project is licensed under the MIT License.