# ValheimFurioso Server
Valheim Furioso's mod collection

Install the server using LinuxGSM.
Install mod support using LinuxGSM.
Copy this folder into the Valheim's server BepInEx folder

Note: If the installation using mods are unable to load your configuration parameters, open /home/vhserver/serverfiles/start_server_bepinex.sh, and modify this line:
exec ./valheim_server.x86_64 ..... (some parameters)
To send the configuration parameters change it for:
exec ./valheim_server.x86_64 "$@"
This basically tells the script to pipe all the attributes from the last script, which in this case are the configuration parameters
WARNING: This change is reset after a LinuxGSM vhserver update