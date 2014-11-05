# The official document is in the hands of marketing now. This is just here for historical purposes. Do not edit me!

The mobile appliance will need an SSL certificate in order to serve secure content. We prefer that you buy these and manage their renewal, but give us access to your account.

- Go to namecheap.com
- Buy a Comodo PositiveSSL Wildcard Cert
- This will cost about $100/year. We recommend that you set up auto-renewal.
- You do not have to generate the CSR! We will take care of all the technical aspects of generating and signing the certificate.
- However, during that technical process, in order to confirm your ownership of the domain, NameCheap will send an email to `admin@youraddress.com`. Go ahead and set this email up now, and point it to yourself.
- Give us the username and password over the phone.
- You'll receive two emails to `admin@youraddress.com` while we're going through our steps. The first will ask you to confirm your address, and the second will have an attachment with the public key. Please confirm the first email, and forward us the second email as soon as you receive it. It typically takes about a day from the moment we submit a CSR for NameCheap to send out the first email, and an hour after you confirm the first until they send out the second.

You'll probably also want to point `mobile.youraddress.com` at the appliance. As with the SSL certificate, we prefer that you buy and manage the renewal of your domain name. Once the appliance is installed at your facility, you'll need to do this. Of course, if we're managing your domain this is something we'll do once we determine the address where the appliance will live, which has to do with your network. For now, to set up the appliance, the only thing we need is to know what the domain name will be. Again, we recommend `mobile.youraddress.com`.

We will also be setting up security access control for your xTuple database. It's our recommendation that you do not allow access to the database from the desktop client from outside of your company's network. You will be able to use the mobile/web client from anywhere, and you will be able to access the database through the desktop client over a VPN if you are working from outside of the office. Let us know if you require desktop connectivity from outside the office and aren't able to use a VPN to secure your communications.

With the mobile framework enabled, you will find it difficult to add data directly into the database using pgadmin, MS Access, ODBC, the API schema, or similar mechanisms. We recommend you use our full-featured REST interface, or CSVimp, for direct data access. Please let us know if you have pre-existing processes set up to insert data directly into your xTuple database, and we will work with you to find a solution.


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