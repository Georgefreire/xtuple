The xTuple Server requires a secure SSL connection for users connecting via the Web client. You will need to obtain an SSL certificate, and configure your domain for outside access in order to prepare to install the xTuple Server for outside access. It can take a few days to obtain an SSL certificate, so it is important to begin this process as soon as possible.

##SSL Certificate##
The xTuple Appliance will need an SSL certificate in order to serve secure content. We recommend you buy a wildcard certificate, so that you may create as many subdomains as you need for pilot sites.

##DNS and IP## 
You'll probably want to set up a domain such as mobile.[youraddress].com to use for the mobile web interface.
Determine the external IP address that you want to map to mobile.[youraddress].com. 
Set up the domain record at your domain registrar.
It can take a day or so for a global DNS record to make its way around the internet.
Set up an internal DNS mapping so that users on your internal network can enter mobile.[youraddress].com and be routed to the correct internal IP. This will most likely be done on your router. 

Important note: is your network set up on a standard internal IP ranges? typical ranges are here:
   - 10.0.0.1 to 10.255.255.254
   - 172.16.0.1 to 172.31.255.254
   - 192.168.0.1 to 192.168.255.254

http://technet.microsoft.com/en-us/library/cc958825.aspx

Make it a standard practice to set a static IP for the appliance
	- set it before install if we can (add to checklist and questionnaire)

The app will run over non-SSL for internal access. External connections will require SSL.

##Security##
We recommend that you do not allow the desktop client to access to your xTuple database from outside your company's network. You can use the mobile/web client from anywhere, and you can use the desktop client over VPN from outside of the office. 