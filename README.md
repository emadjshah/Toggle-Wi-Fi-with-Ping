# Toggle-Wi-Fi-with-Ping


This is a batch script that toggles the enabled/disabled state of a network interface (in this case, the Wi-Fi interface) based on the result of a ping to the Google DNS server at 8.8.8.8.

The first few lines of the script attempt to check whether the script has administrative privileges. If it does not, it will try to request them by invoking a VBScript file that prompts the user for permission to run the script as an administrator.

After this, the script uses the ping command to send a single packet to the Google DNS server. Depending on whether the ping is successful or not (i.e., whether there is a response from the server), the script will either enable or disable the specified network interface using the netsh command.

Note - If you're using `Ethernet` then change `Wi-Fi` to `Ethernet 3`
