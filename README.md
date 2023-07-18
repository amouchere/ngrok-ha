# NGROK Homeassistant



## Ngrok installation

On raspberry pi :
```
 curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | \
  sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null && \
  echo "deb https://ngrok-agent.s3.amazonaws.com buster main" | \
  sudo tee /etc/apt/sources.list.d/ngrok.list && \
  sudo apt update && sudo apt install ngrok
```

## Installation

```
git clone
```

Edit the ngrok-ha.yml file to set the ngrok token and the basic auth configuration.

## Enable ngrok-ha.service

To launch ngrok-ha as a service, do :

```
sudo cp ~/ngrok-ha/ngrok-ha.service /etc/systemd/system/ngrok-ha.service
sudo systemctl enable ngrok-ha.service
sudo systemctl start ngrok-ha.service
```