# SimpleTimeService
Simple Time Service is a lightweight Flask-based application which returns the current timestamp along with the Server's IP address.

# Prerequisites
# 1. AWS EC2 Instance
# 2. Docker
   Docker must be installed on your system or VM. To set up Docker in your virtual machine, run below commands:
      sudo yum install docker -y
      sudo systemctl start docker
      sudo systemctl enable docker
      sudo usermod -aG docker ec2-user
      exit and re-connect to VM
# 3. DockerHub Account
  You will need a DockerHub account to pull the image.

# Steps to Run the Application
<h3> Step 1: Pull simpletimeservice Docker Image from docker hub by passing below command: </h3>
          docker pull ankitasingh7/simpletimeservice:V1
<h3> Step 2: Now, Create container based on “simpletimeservice” image by passing below command:</h3>
          docker run -d -p 9000:9000 ankitasingh7/simpletimeservice:V1
<h3> Step 3: Configure Security Group </h3>
        Go to security group in ec2 machine and expose port 9000 to access to the application.
<h3> Step 4: Access the Application </h3>
        Access the Application, open a browser and pass IP:exposed host (eg-  http://54.151.93.185:9000/) </br>
	      application will be running on port num: 9000



