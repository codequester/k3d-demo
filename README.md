# [K3d - How to run Kubernetes cluster locally using Rancher k3s](https://youtu.be/mCesuGk-Fks)

k3d and Podman can be used together, but support for Podman is experimental and k3d is not guaranteed to work with it: 

- Compatibility: k3d uses the Docker API and is compatible with Podman v4 and higher. 
- Using Podman with k3d: To use Podman with k3d, you can: 
  1. Ensure the Podman system socket is available by running sudo systemctl enable --now podman.socket 
  2. Create a symbolic link to point k3d at the right Docker socket by running ln -s /run/podman/podman.sock /var/run/docker.sock 
  3. Set DOCKER_HOST when running k3d by running export DOCKER_HOST=unix:///run/podman/podman.sock
