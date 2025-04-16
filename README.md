# 1. Update system packages
sudo yum update -y

# 2. Install Java (Jenkins requires Java)
sudo yum install -y java-17-openjdk

# 3. Add the Jenkins repo
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo

# 4. Import the Jenkins GPG key
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key

# 5. Install Jenkins
sudo yum install -y jenkins

# 6. Enable and start the Jenkins service
sudo systemctl enable jenkins
sudo systemctl start jenkins

# 7. Check Jenkins status
sudo systemctl status jenkins
