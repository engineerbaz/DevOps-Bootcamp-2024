# Installation & Setup of Docker

## Remove Older Version
```
sudo apt-get remove docker docker-engine docker.io containerd runc
```

## 1. Set up the Repository
Update the apt package index and install packages to allow apt to use a repository over HTTPS:

```
sudo apt-get update
```
```
sudo apt-get install ca-certificates curl gnupg
```

## 2. Add Docker’s official GPG key:

```
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

## 3. Use the following command to set up the Repository:
```
echo “deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

## 4. Install Docker Engine:
```
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
## 5. Verify that the Docker Engine installation is successful by running the hello-world image:

```
sudo docker run hello-world
```
