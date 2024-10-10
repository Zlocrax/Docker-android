hello this is my way of getting a docker like env on mobile to run python/node.js bots for adavanced devs only

you need to get root access in a terminal like application (termux) ubunutu or my kali installer is probaly to best and easiest ways to do so.

after you get root access create a dir called bots so you can keep an eye on them 

move your bot folders into this dir 

create venv in the directory 

then when you start your bot use one of these cmds

nohup &

setsid 

disown 

pm2

now your bot is in its own docker like env running forever until you turn it off nohup & is the best one in my opinion 

enjoy
