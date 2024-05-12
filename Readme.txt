sudo apt update
sudo apt install maven -y
sudo apt install python3
sudo apt-get install unzip
sudo apt install -y nodejs npm
sudo npm install -g express
sudo npm install express
sudo apt install python3-selenium -y
sudo npm install puppeteer
sudo npm install webdriverio
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins -y
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt update
sudo apt install google-chrome-stable -y


# Example: For Chrome 123.x, use the corresponding ChromeDriver
wget https://storage.googleapis.com/chrome-for-testing-public/123.0.6312.122/linux64/chromedriver-linux64.zip
unzip chromedriver-linux64.zip
sudo mv chromedriver-linux64 chromedriver
cd chromedriver
sudo mv chromedriver /usr/bin/

sudo chown root:root /usr/bin/chromedriver
sudo chmod +x /usr/bin/chromedriver

google-chrome

dockerfile config
sudo chmod 666 /var/run/docker.sock
sudo docker build -t nodecalci .  (inside project directory)
sudo docker run -d -p 5000:3000 nodecalci


Anisble setup
sudo apt update
sudo apt install ansible -y
as it will not generate ansible directory inside /etc
sudo mkdir -p /etc/ansible
sudo touch /etc/ansible/hosts
sudo nano /etc/ansible/hosts
[servers]
54.209.198.11
ansible servers -m ping
it will not do ping pong
then go to cd .ssh
sudo ssh-keygen
then add open new id_edXXXX.pub file copy its whole line and
add it into authorized_key in same directory in next line
similar can be done if using two different server 
now do ansible servers -m ping
it will pong
learn shell for ansible
ansible -i inventory.yml all -m "shell" -a "touch sell1.yml"
