# Requirements/Inputs

## 1. What edition is the customer on? 

- Postbooks
- Manufacturing
- Distribution
- Enterprise

## 2. What other products has the customer bought?

- eCommerce
- BI
- XTN
- Other

## 3. What version are they using? (default to latest tag)

## 4. What are the customer's qt remote access expectations?

- Unsecured remote access (despite our warnings)
- VPN remote access
- No remote access

## 5. What are the customer's internal network IP ranges?
- Make it a standard practice to set a static IP for the appliance
- set it before install if we can 
- how to set it after install?

## 6. What is the customer's DNS plan?
- Host DNS locally
- Be okay with the app being inaccessible even from within the office if the Internet is out
- Authorize us to allow the app to run over non-SSL for internal access (requires that their network ranges are set up with one of the correct internal IP ranges)

## 7. Do we already have a database backup to start with?

## 8. What flavor of database are we going to be installing?

- Empty
- Quickstart
- The `.backup` file is already prepared

## 9. What is the domain on which the mobile app will be hosted?
- this must be the same domain that the SSL cert validates

## 10. Locale Information
- Country
- Timezone
- Language

Questionnaire key: (TODO)
1&2:
distribution: [inventory, distribution],
manufacturing: [inventory, manufacturing],
enterprise: [inventory, distibution, manufacturing, (masterref)],
bi: [bi extension, bi repository],
ecommerce: [xdruple]

- We also need the cert, the private key, and the bootstrap script to be on the appliance.

- We'll need a backup on the appropriate version. Even for new customers, they'll have a backup that the implementor has loaded with some data. (Perhaps in the future we might want to load data onto the database after the appliance is built? We'd also have to think about their packages and their license key in that case. For now, we assume that the database has everything it needs except mobile.)

