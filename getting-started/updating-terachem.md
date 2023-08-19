# Updating TeraChem

Users with IP-Checkout licenses can update TeraChem from the command line by running

```
terachem --update
```

In this case the newest release will be downloaded, verified, and saved in the working directory:

```
TRYING THE NETWORK LICENSE...
Connecting to license server ’54.208.252.40’ port ’8877’...
Connected!
Checking your license...
Download started... done
Verifying... OK
The installer has been saved as tc1.93P.tar
```

In order to prevent potential data corruption issues, it is recommended to install the release in another directory and then follow the standard installation procedure described in Sec. 2.2. If a newer version is available, TeraChem notifies the user on startup:

```
TRYING THE NETWORK LICENSE...
Connecting to license server ’54.208.252.40’ port ’8877’...
Connected!
Checking your license...
**************************************************************
Greetings, Todd Martinez! You have 2 licenses in total
IN USE: 0
AVAILABLE: 2
ATTENTION: A NEWER TERACHEM VERSION (v.1.93) IS AVAILABLE
TO UPGRADE, PLEASE RUN ’terachem -u’ OR CONTACT PETACHEM
**************************************************************
```

Neither version checking nor command line updating is available for users with node-locked licenses, because then TeraChem is not allowed to access the Internet. Users with node-locked licenses should contact PetaChem to obtain the latest release.
