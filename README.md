# Docker Compose script for NEURONE deploy

This is a simplified script to deploy NEURONE using Docker Hub images. A GNU/Linux 64bit operating system with internet connectivity is required to run this script.

## Install Instructions

Example instructions are for Ubuntu Server, adapt accordingly to your GNU/Linux distribution:

1. In your machine, install Docker:

        $ sudo apt-get update
        $ sudo apt-get install apt-transport-https ca-certificates curl software-properties-common unzip
        $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
        $ sudo apt-key fingerprint 0EBFCD88
        $ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
        $ sudo apt-get update
        $ sudo apt-get install docker-ce

2. Enable Docker for your current user (so you don't need `sudo` anymore):

        $ sudo usermod -aG docker $(whoami)
        $ logout

3. Install Docker Compose:

        $ sudo apt-get update
        $ sudo apt-get -y install python python-pip
        $ sudo pip install docker-compose

4. Clone this repository (or download it as ZIP)

5. Enter to the script directory (e.g. `cd neurone-docker`)

5. To start NEURONE, run `./neurone-start.sh` on terminal (`sudo` permissions may be required to set folder permissions)

6. To stop NEURONE, run `./neurone-stop.sh` on terminal

## License

This script is released under AGPLv3

All other dependencies are available under their own licenses