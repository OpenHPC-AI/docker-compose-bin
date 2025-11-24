# docker-compose-bin

**Installing Docker Compose (if not already present):**

**On Linux (as a plugin):**

If you've installed Docker Engine using the official Docker repository method, Docker Compose (as a plugin) should be installed automatically. You can verify this by running:

```bash
docker compose version
```

If it's not present or you need to install it manually:

```bash
sudo curl -L https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

**Enabling Docker Compose:**

Docker Compose, when installed as a plugin, is inherently "enabled" as part of your Docker installation. There is no separate service to start or enable for Docker Compose itself. You use it directly via the docker compose command.

To enable the Docker daemon to start automatically on system boot (relevant for Linux):

While not directly for Docker Compose, ensuring the Docker daemon starts automatically is crucial for using Docker Compose without manual intervention after a system reboot.

```bash
sudo systemctl enable docker
sudo systemctl start docker
```
3. Verifying the Installation:

After installation, verify Docker Compose is working correctly:

```bash
docker compose version
```
