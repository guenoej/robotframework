# Documentation for Robot Framework
#### Repository for the step-by-step installation of the robot framework and its dependencies.
   
### GitHub

 **Install GitHub**
 
    sudo apt-get update

    sudo apt install git
    
  **Check GitHub Version**

    git --version

  **Set User Name Global**

    git config --global user.name {seu.user.name}
    
  **Set User Email Global**

    git config --global user.email	{seu.user.email}
    
  **Check GitHub User**

    git config --list
    
  **Set SSH Agent**

    ssh-keygen -t ed25519 -C "{seu.user.email}"
    
  **Set SSH Agent**

    ssh-keygen -t ed25519 -C "{seu.user.email}"

  **Set SSH Agent 'No algorithm support Ed25519'** 
  
  <sub> If the command fails and you get an invalid format or feature not supported error, you may be using a hardware security key that does not support           the Ed25519 algorithm. Enter the following command. </sub>
    
    ssh-keygen -t rsa -b 4096 -C "{seu.user.email}"
    
  **New SSH key** 
  
  <sub> Copy the generated key value inside the ".ssh" </sub>
      
    Open GitHub >> Settings >> SSH and GPG keys >> New SSH key
    
  **Title**

    Ex. Dell Inspirion
    
  **Key type**

    Authentication Key
    
  **Key**

    Paste the generated key value inside the ".ssh"
    
    Add SSH key
    
  **Copy URL SSH**
  
    Open Repository >> <> Code >> SSH >> Copy URL
    
  **Clone Repository Over SSH**

    git clone {URL_SSH}

### Python and NPM

 **Install Python**

    sudo apt-get install python3

 **Install Pip**

    sudo apt-get install python3-pip 
 
 **Install Curl**

    sudo apt install curl

 **Install Wget **

    sudo apt install wget
    
 **Install NPM**

    sudo apt install npm
       
    wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash 

    source ~/.profile

 **Listing available versions of Node.js**

    nvm ls-remote

 **Installing Node.js version and setting default**

    nvm install v15.0.0
    
	  nvm use v15.0.0
    
	  nvm alias default v15.0.0
    
	  nvm alias default node

### Robot Framework and its dependencies

 **[Robot Framework](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html)**

    pip install robotframework
    
 **[Requests Library](https://marketsquare.github.io/robotframework-requests/doc/RequestsLibrary.html#POST)**

    pip install robotframework-requests

 **[Browser Library](https://marketsquare.github.io/robotframework-browser/Browser.html)**

    pip install robotframework-browser
    
    rfbrowser init

<sub> You may need to restart your computer </sub>
    
 **[JSON Library](https://robotframework-thailand.github.io/robotframework-jsonlibrary/JSONLibrary.html)**

    pip install robotframework-jsonlibrary

 **[Pabot](https://pabot.org/)**

    pip install robotframework-pabot

### Docker

  **Set up the repository**
  
    sudo apt-get update
    
    sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
    
  **Add Docker’s official GPG key**

    sudo mkdir -m 0755 -p /etc/apt/keyrings
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

  **Use the following command to set up the repository**
  
    echo \
    "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    
  **Update the apt package index**
  
    sudo apt-get update
    
  **Install Docker Engine, containerd, and Docker Compose**
   
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    
  **Set Docker User**    
  
    sudo groupadd docker

    sudo usermod -aG docker ${USER}
    
  **Permission Directory Docker**
  
    sudo chmod 666 /var/run/docker.sock
