# Databox Container Manager
Databox OS container manager and dashboard server.

## Installation

###Linux
    Install docker https://docs.docker.com/engine/installation/linux/
		Install nodejs https://nodejs.org/en/download/

		For now the arbier IP must be in you hosts file

	  echo "172.17.0.3     databox-arbiter" | sudo tee -a /etc/hosts
	  echo "172.17.0.2     databox.registry" | sudo tee -a /etc/hosts

###OSX
    Install docker https://docs.docker.com/docker-for-mac/
		Install nodejs https://nodejs.org/en/download/

		For now the arbier IP must be in you hosts file

    edit /etc/hosts and add 127.0.0.1 databox-arbiter
    edit /etc/hosts and add 127.0.0.1 databox.registry

###Windows
		Install docker https://docs.docker.com/docker-for-windows/ (The old Docker Toolbox is not supported)
		Install nodejs https://nodejs.org/en/download/

		For now the arbiter IP must be in you hosts file

	  edit :\Windows\System32\Drivers\etc\hosts and add 127.0.0.1 databox-arbiter
	  edit :\Windows\System32\Drivers\etc\hosts and add 127.0.0.1 databox.registry

###All

     git clone https://github.com/me-box/databox-container-manager.git
	   cd databox-container-manager
	   npm install --production


## Usage

In production mode (remote docker registery and remote app store)

	npm start

In development (local docker registery and local App store)

  DATABOX_DEV=1 npm start

	Note: in dev mode some extra configuration is required. Follow the on screen instructions.  

Default port is 8080, but can be overridden using the PORT environment variable, i.e.:

	PORT=8081 npm start

Then browse to http://localhost:8080/.
