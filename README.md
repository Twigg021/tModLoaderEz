# tModLoaderEz

Planning


Mod installing should allow for download links directly to .tmod files as well as steam workshop IDs.  Not sure how the API works with IDs but if it allows for specific version queries then allow that with <Mod ID>:<Version ID>



Download
Install
Set bash or whatever to use tModLoaderEz as a command that starts main.js
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
4. Update {Just reruns startup scripts to update everything}
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
Each setting here should automatically pull from their config.  If not set, it should ask the user  

1. 
