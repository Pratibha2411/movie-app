### Steps to do:
  sudo apt install nodejs
  sudo apt install npm
  npm install
  npm start 


### Steps for CI/CD:
  
Create AWS EC2 instance
sudo apt update
sudo apt install openjdk-11-jre
java -version
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io.key | sudo tee \   /usr/share/keyrings/jenkins-keyring.asc > /dev/null 
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \   https://pkg.jenkins.io/debian binary/ | sudo tee \   /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update 
sudo apt-get install jenkins
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
sudo cat /var/lib/jenkins/secrets/initialAdminPassword  
sudo apt install docker.io

### Dockerfile: 

FROM node:12.2.0-alpine 
WORKDIR app 
COPY . . 
RUN npm install 
EXPOSE 8000 
CMD ["node","app.js"]

docker build . -t node-app 
sudo usermod -a -G docker $USER 
docker run -d --name node-todo-app -p 8000:8000 todo-node-app

### Features needed to work on
need to work on Button-AddFavBtn && RemoveBtn
container flex-wise
Show the name of the Movies, Genr
User should be able to add movies (name, description, cast, similar movies, genre, language, etc.)
Users should be able to search movies by name, and genre.
Users should be able to filter movies by language
README file with proper details.
proper comments in the function/block of the code.