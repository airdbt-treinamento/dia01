   ~$  sudo apt-get update && sudo apt-get upgrade -y
   
   ~$  sudo apt remove docker-desktop
   ~$  rm -r $HOME/.docker/desktop
   ~$  sudo rm /usr/local/bin/com.docker.cli
   ~$  sudo apt purge docker-desktop
   
   ~$  sudo apt-get install -y git neofetch ca-certificates curl gnupg lsb-release
   
   ~$  sudo apt-get update && sudo apt-get upgrade -y
   
   ~$  sudo mkdir -p /etc/apt/keyrings
   ~$  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
   ~$  echo   "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   
   ~$  cat /etc/apt/sources.list.d/docker.list
   
   ~$  apt-cache madison docker-ce | awk '{ print $3 }'
   
   ~$  sudo apt-get update && sudo apt-get upgrade -y
   
   ~$  sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
   
   ~$  sudo groupadd docker
   ~$  sudo usermod -aG docker $USER
   ~$  newgrp docker
   
   ~$  docker --version
   ~$  docker compose version
   ~$  sudo systemctl status docker.service
   
   ~$  sudo reboot
   
   ~$  neofetch
