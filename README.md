# WordPresss-site
This is for creating a wordpress site using docker compose for assignment given by rtCamp organization.

Step 1: Installing Docker Engine
  First, install required dependencies using the following command:
  apt-get install apt-transport-https curl ca-certificates curl software-properties-common -y

  Next, add Docker’s GPG key using the command below:
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -

  Next, add the Docker repository to the APT source file.
  add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

  Finally, install the latest version of Docker using the command below:
  apt-get install docker-ce -y

  Once the Docker is installed, verify the Docker version using the following command:
  docker --version

Step 2: Installing Docker Compose
  Run the following command to download the current stable release of Docker Compose:
  curl -L https://github.com/docker/compose/releases/download/1.29.2/docker-compose-Linux-x86_64 -o /usr/local/bin/docker-compose

  Next, set the executable permission to the downloaded binary:
  chmod +x /usr/local/bin/docker-compose

  verify the Docker-compose version using the following command:
  docker-compose --version

Step 3: Setting Up YML File
  First, create a WordPress directory to hold your docker-compose.yml file:
  mkdir wordpress

  Next, create a docker-compose.yml file using the following command:
  vi wordpress/docker-compose.yml

Step 4: Building WordPress Container
  First, change the directory to wordpress:
  cd wordpress

  Next, start both containers using the pre-defined values:
  docker-compose up -d

  You can check both container images downloaded by the dokcer-compose.yml file using the command below:
  docker-compose images

  Next, verify the running container with the following command:
  docker-compose ps

  To check the WordPress container logs, run:
  docker-compose logs wordpress

  To check the Database container logs, run:
  docker-compose logs database

Step 5: Getting Access to WordPress Website
At this point, your WordPress site is ready. Now, open your web browser and type the URL http://your-server-ip. You will be redirected to the WordPress language selection screen.

Step 6: Updating WordPress Container
  First, stop all containers using the following command:
  cd wordpress
  docker-compose down

  Next, download the latest version of WordPress and MySQL image using the following command:
  docker-compose pull

  Next, create and launch both container using the following command:
  docker-compose up -d

Conclusion
  Your WordPress website is now up and running in a containerization environment. I hope you have now enough understanding of how Docker Compose works and helps you to set up a WordPress website within a minute.




