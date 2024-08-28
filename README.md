# Docker and Docker Compoose Tutorial


This is the tutorial
https://www.youtube.com/watch?v=gAkwW2tuIqE&t=175s


## Create a Docker Container with a Web App


0. Go to the working directory
```
cd src
```

1. Initialize a Node.js project
```
npm init -y
```

2. Install Express
```
npm install express
```

3. Add a custom script to run your application
```
"scripts": {
  "start": "node index.js"
}
```
4. Build the docker image
The scottmillers is my GitHub account id.
```
 docker build -t scottmillers/demoapp:1.0 .
```

5. Run the container based on the image
```
docker run -p 5000:8080 scottmillers/demoapp:1.0 
```

6. Access the containers running web server
If you are running in a container you need to go to the host machine.
```
curl localhost:5000
```

## Create a Docker Compose Application

Steps
1) Create a docker-compose.yml file
2) Add a web and mysql image
3) Run it
```
docker-compose up
```


