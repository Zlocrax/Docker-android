Hello this is my way of building a docker like env on mobile to succesfully deploy python bots and/or applications FOR ADAVANCED DEVS ONLY

This is for both rooted and rootless devices

First you need to get root access in a termux

The easiest way is like this(copy and paste 1by1):

pkg install git -y

git clone https://<i></i>github.com/hctilg/root-termux.git && cd root-termux && chmod +x *

pkg install wget proot -y

yes | bash install.sh

bash start.sh

apt update

apt upgrade

apt install sudo

With thanks to https://github.com/hctilg for that part 

fyi this way also works with my nethunter installer as that also gives you root access

Now onto my steps(copy and paste 1by1):

sudo apt install wget libncurses5-dev build-essential zlib1g-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev libbz2-dev pkg-config -y

sudo apt update && sudo apt full-upgrade -y

Once that is complete you must also compile python.

Continue following my steps(copy and paste 1by1):

wget https://<i></i>www.python.org/ftp/python/3.12.2/Python-3.12.2.tgz

tar -xf Python-3.12.*.tgz

cd Python-3.12.*/

./configure --enable-optimizations

leave it to do its thing now lets build python

make -j $(nproc)

sudo make altinstall

Once complete check your python version with

python3.12 --version

now lets install and build pip(copy and paste):

curl -sS https://<i></i>bootstrap.pypa.io/get-pip.py | python3.12

Check pip version with, pip3.12 -V and use sudo pip3.12 install to install with pip

Now python is compiled and built you now can move your bot scripts/files into root-termux or create a new dir called bots

After you have changed directory into your bot files you must create a venv env with 

python3 -m venv .venv && source .venv/bin/activate

Now install your pip requests and modules 

After Everything is installed and needed for your bot to run please use one of the cmds down bellow before you input your cmd to deploy your bot and do not deactivate the venv

nohup &

setsid

disown

pm2

After your bot is deployed please click require wakelock on the termux notification 

Now your bot is in its own docker like env running forever until you turn it off nohup & is the best one in my opinion


thank you and enjoy

-ZłO

![1000485377](https://github.com/user-attachments/assets/487db380-9c2a-4d31-92bf-2b2c91dab1ab)
![1000485551](https://github.com/user-attachments/assets/183adcbd-8696-446e-b6cd-7ae95fa59db1)
![1000485549](https://github.com/user-attachments/assets/13db350b-7f09-4d11-b197-9d6320fd065f)
