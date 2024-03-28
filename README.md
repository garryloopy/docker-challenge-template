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
