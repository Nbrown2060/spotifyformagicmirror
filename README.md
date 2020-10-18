# spotifyformagicmirror
A simple Repository for having Spotify on MagicMirror

# First:

Make sure you have the latest MagicMirror Version. You can check by doing 
> cd ./MagicMirror && git pull && npm install

# 2nd: 


> sudo apt install -y apt-transport-https curl
> curl -sSL https://dtcooper.github.io/raspotify/key.asc | sudo apt-key add -v -
> echo 'deb https://dtcooper.github.io/raspotify raspotify main' | sudo tee /etc/apt/sources.list.d/raspotify.list
> sudo apt update
> sudo apt install raspotify


To configure go to:
> sudo nano /etc/default/raspotify

There you can change your Mirror's name and bitrate
FOR THIS TO WORK DO NOT EDIT THE FOLLOWING LINE IN THE CONFIG FILE!
> OPTIONS="--username <USERNAME> --password <PASSWORD>"
  
  Then:
  > sudo systemctl restart raspotify
  
  
  # 2nd Part:
  
  # First:
  
  > cd modules
> git clone https://github.com/raywo/MMM-NowPlayingOnSpotify.git
> cd MMM-NowPlayingOnSpotify
> npm install
  
 > cd authorization
> node app

When the app is running you can access it by opening localhost:8888 in your browser. Provided you are doing this directly on your Raspberry Pi. If you want to access the app remotely just type the ip address or the name of your Raspberry like so for instance: http://raspi:8888. 
Now just follow the steps described there. After successful authorisation the app will display a code snippet under the heading Step 3: Configure your mirror. Copy that snippet and paste it into your mirror’s config.js. Configure the rest to your needs and you’re good to go.


Any Questions? Email me at nathanielbrown2060@gmail.com
DISCLAMER: I DID NOT CREATE RASPOTIFY OR NOW PLAYING ON SPOTIFY, THIS IS SIMPLY A GUIDE!
ORIGINAL AUTHORS NAMES BELOW:

https://github.com/raywo/MMM-NowPlayingOnSpotify
https://github.com/dtcooper/raspotify
