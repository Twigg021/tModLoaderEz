# tModLoaderEz

Planning


Mod installing should allow for download links directly to .tmod files as well as steam workshop IDs.  Not sure how the API works with IDs but if it allows for specific version queries then allow that with <Mod ID>:<Version ID>



Figure out which of these are actually needed  

sudo chown -R $USER:$USER /home/ubuntu/tMod-ServerManager/tMod-Server  
chmod +x /home/ubuntu/tMod-ServerManager/tMod-Server/dotnet/dotnet  
chmod +x /home/ubuntu/tMod-ServerManager/tMod-Server/start-tModLoaderServer.sh  
chmod -R 755 /home/ubuntu/tMod-ServerManager/tMod-Server/tModLoader-Logs  




Download  
Install  
Set bash or whatever to use tModLoaderEz as a command that starts main.js (Ask User)  
tModLoaderEz >> node main.js  





# Startup

Check config for needed node packages  
Check currently installed packages  
Compile list of needed packages  
If mismatch, ask User if they would like to install them (Closes if they answer no)

Check config for desired tModLoader version ('Custom' stops this check here, 'Latest' is default)  
Check latest stable on GitHub if 'Latest'  
Check if current version matches desired  
If mismatch, ask User if they would like to install the desired version  

Check config for current version of all downloaded mods (only Mod ID based ones, ignore direct download links and ones with a specific version set)
Check steam for current versions
Check if downloaded versions matches current versions
If mismatch, ask User if they would like to update them






# Main Menu


===tModLoaderEz===  
<Server Active/Server Inactive> - <Public-IP>:<Port>  
0. Active Server Manager {Only displays if Server Active}  
1. Start Server (Auto)      --> Stop Server (Auto)  
2. Start Server (Manual)    --> Stop Server (Manual)  
3. Mod Editor  
4. Update {Cleanly pulls the server down and reruns startup script.  In settings can be set to run automatically on a timer.}
5. Settings  



# Active Server Manager

(-) Runs tModLoader server commands, IE: -help  
(.) Runs tModLoaderEz commands, IE: .help  
(.exit) returns to main menu  



# Mod Editor
This should pull from/ interact with two different configs.  One for 'Downloaded Mods', and another for 'Installed Mods'  

1. List Mods  
2. Add Mods  
3. Remove Mods
4. Update Mods {Allows the User to update mods installed by download link or update only specific mods for if they chose No on startup update all mods}  
5. Deactivate All  
6. Activate All  
7. Back {If the server is active, it should ask the user if they would like to restart it}



# Start Server (Auto)
Each setting here should automatically pull from their config.  If not set, it should ask the User  

1. Use steam server (y/n):  
2. Choose World (#/n): {If no config set, this will need to wait for the actual server setup to query, as it will show which #s are avaliable since they're pulled from found world files}
   #: Move on
   n:
     a. Choose size (1/2/3):  
     b. Choose difficulty (1/2/3/4):
     c. Choose world evil (1/2/3):
     d. Enter world name:
     e. Enter Seed (Leave Blank For Random):
     Then auto select the highest number, since this will return to 'Choose World' and the highest number will be the newest world
3. Max Players (1-16):
4. Server Port:
5. Automatically forward port? (y/n):
6. Server password (press enter for none):



# Start Server (Manual)
Run the same set as Auto, but ignore config and ask for entry on everything
