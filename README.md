# SinusBot startscript

## Installation

1. Copy the file `sinusbot.service` to `/lib/systemd/system/sinusbot.service`
2. Adjust the following placeholders to your installation:
  
   placeholder                   | description                                 | example
   ------------------------------|---------------------------------------------|------------------------
   YOUR_USER                     | Your user who starts the bot                | sinusbot               
   YOURPATH_TO_THE_BOT\_BINARY   | Your path to the SinusBot binary            | /opt/sinusbot/sinusbot 
   YOURPATH_TO_THE_BOT_DIRECTORY | Your path to the SinusBot install directory | /opt/sinusbot          
  
3. Load SinusBot only if ts3server.service is loaded (optional): Uncomment `#Requires=ts3server.service`
4. Reload systemd: `systemctl daemon-reload`
5. Enable autostart (optional) `systemctl enable sinusbot`
6. Start the sinusbot: `systemctl start sinusbot`
