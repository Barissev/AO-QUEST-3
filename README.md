# HI, Today we will look at how to do the 3rd task on AO. Server specifications are not important, you can install it on the lowest-priced server.

# Let's update the server.

```
sudo apt update -y && sudo apt upgrade -y
```
# Enter the codes one-by-one.
```
curl -sL https://deb.nodesource.com/setup_20.x -o /tmp/nodesource_setup.sh
sudo bash /tmp/nodesource_setup.sh
sudo apt install nodejs
```
# Same, one-by-one.
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
source ~/.bashrc
nvm install v20.10.0
nvm use v20.10.0
npm install -g npm@latest
```
# Let's Install AO
```
npm i -g https://get_ao.g8way.io
source ~/.bashrc
```
# Download Discord to your Server.

```
npm install discord.js ws @permaweb/aoconnect fs
```

# Let's create a Folder called DevChat in Root.
```
mkdir -p /root/DevChat/src/
```

# You should download the Lua extension to your server and enable it for the root folder. (I am using VSCode and recommending it.)


# Let's check if you have all the files, if not you can copy it from my repo but don't forget to replace the correct fields with your own PID and your own Discord Bot Token ID, Discord Channel ID.

```
cd /DevChat/src/
ls -a
```

# You should see the followin files capture.js , index.js , process.lua , client.lua , chatroom.lua , router.lua

# MOST IMPORTANT POINTS:
# Go to Chatroom.lua and Change StanbeornRoom = StanberonRoom to your own name.
# Go to index.js change const token ="x" to your Discord BOT Token.
# Go to Discord, enable Discord Developer Mode, copy your General Chat ChannelID and change it as well.
# When you start AOS down below, you will get a PROCESS ID. You will see process: 'x' in the index.js file. Change it with it.
# Do not change other files at all.


#Let's start AOS

```
aos
```

#Copy your ProcessID(PID).

# Let's register to the chatrooom.

```
ao.send({ Target = "xnkv_QpWqICyt8NpVMbfsUQciZ4wlm5DigLrfXRm8fY", Action = "Register", Name = ao.id })
```

# Let's send a message. (Do not change)
```
Say("Hello, this is a first test message.", ao.id) 
```
# Open 2 more terminals.

# First enter the code below:
```
node /root/DevChat/src/index.js
```
# Second enter this code:
```
node /root/DevChat/src/capture.js
```
# Lastly, broadcast this message if you can see this message both on Discord and terminal, well done!
```
Say("Hello, this is a test message.", ao.id)
```


