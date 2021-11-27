- Create a directory for the frontend html code

- Create a Dockerfile

- pull the httpd webserver from the hub
` FROM httpd:alpine `

- copy the frontend source code from the host to the container directory where apache will load the website from
` COPY ./html/ /usr/local/apache2/htdocs/ `

# To Build
` docker build -t my-website:1.0 . `

To run the image in a container
docker run -d -p 8080:80 --name my-website-container my-website:1.0