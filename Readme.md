
# docker important points
1. cd /path/to/your/project

2.  docker build -t my-blog .

3. docker run -p 8000:8000 my-blog // it will run the container from the my-blog image

4. docker ls

5. docker ps

6. docker stop conatiner id

7. docker images

8. docker stop backend-dev  // for stop container with name backend-dev


89. docker rm backend-dev // remove from history


note-: after docker stop container id

note-: docker start backend-dev 
insted of  docker run -d -p 9000:8000 --name backend-dev saurav0503/my-blog because backend-dev container name is already exist



note-: my-blog is docker image name

note-: It maps port 8000 on your local machine to port 8000 inside the container

# ssh Important points
1. cd downloads

2. chmod 400 your-key.pem
3. ssh -i "your-key.pem" ec2-user@<your-ec2-public-ip>
# or for Ubuntu instance
ssh -i "your-key.pem" ubuntu@<your-ec2-public-ip>

4. sudo apt update
sudo apt install nodejs npm git -y
node -v
npm -v

5. git clone <your-backend-repo-url>
cd your-backend-folder

note-: If your project is not in Git, you can use scp to copy files from your local to EC2:
 ans-: scp -i your-key.pem -r ./your-backend-folder ubuntu@<your-ec2-ip>:~/backend

6. cd backend
npm install

7.node server.js
# OR
npm start

8. pm2 is optional for good for manual deployment it always make connection alive unless forcefully stop

9. pm2 start app.js
10. pm2 stop app.js

note-: for manual deployment on ec2 make chnages in file git push and perform step like pull and start server

note-: in automate you just need to push in target branch automtic pipeline will trigger and your code push into ec2 and restart the server

# setup EC2 for docker deploy

1.ssh -i your-key.pem ubuntu@your-ec2-ip

2.sudo apt update
sudo apt install docker.io -y
sudo usermod -aG docker ubuntu
newgrp docker






