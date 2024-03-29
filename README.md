# docker-challenge-template

Challenge 1
The steps are.

1. Create a public folder in the challenge 1 directory.
2. Create a index.html file in the newly created public directory.
3. Create an html template that displays the student name and id.
4. Within the challenge1 directory, create a "Dockerfile" file and add the following lines of codes:
   FROM nginx:latest
   COPY ./public /usr/share/nginx/html
   This ensures that the docker file uses the official NGinx image and copy the contents of the "./public" into NGinx's default HTML directory.
5. Within the root folder run the command: docker build -t challenge-1 ./challenge1
   This command builds a Docker image named "challenge-1" using the Docker file from the directory of "./challenge1"
6. Run the command: docker run -d -p 8080:80 challenge-1.
   This command will start a Docker container based on the "challenge-1" image nad map port 8080 on my local host machine to port 80 inside the container.

Challenge 2
The steps are.

1. Move the required files into challenge2 folder
2. Create a Dockerfile and define how to build the Docker image for the Node.js server
3. Create an nginx folder within challenge2 and place an nginx.conf file inside it, this will configure nginx for us
4. Configure nginx.conf to listen on port 8080 and forward requests to the Node.js server running on port 3000
5. Create a docker-compose.yml file in challenge2 folder.
   Define two services for Node.js and one for Nginx.
   Configure port mapping in the docker-compose.yml file to expose port 3000 for the Node.js server and port 8080 for Nginx
6. Run this command "docker-compose up --build" within the root folder for challenge2
7. Access in the web browser "http://localhost:3000/api/books"
