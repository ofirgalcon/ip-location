IP Location Module
==============

Provides IP location information for clients, including geographical and organizational data.

Data can be viewed under the IP Location tab on the client details page or using the IP Location list view.

Configuration
---
This module uses the [ipinfo.io](https://ipinfo.io/) API to gather location data. You will need to:

1. Register for an API token at https://ipinfo.io/
2. Create a plist file at `/Library/Preferences/com.gal.iplocation.plist` with your token:
   ```bash
   sudo defaults write /Library/Preferences/com.gal.iplocation.plist Token "your_token_here"
   ```

Table Schema
---

* ip - varchar(255) - IP address
* hostname - varchar(255) - Hostname
* city - varchar(255) - City
* region - varchar(255) - Region/State/Province
* country - varchar(255) - Country
* location - varchar(255) - Geographical location coordinates
* organization - varchar(255) - Organization/ISP
* postal_code - varchar(255) - Postal/ZIP code
* timezone - varchar(255) - Timezone

Widgets
---
This module provides the following widgets:

* IP Location City
* IP Location Region
* IP Location Country
* IP Location Organization
* IP Location Postal Code
* IP Location Timezone
