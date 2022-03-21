
## CSO site verification runner.json
This runner will query site deployment in CSO making sure it follows correct order (configure, bootstrap, zero, service provisioning, auto-nat/sdwan/fw and dhcp update for WAN_0/1.

**Required**

***job_id*** environmental variable

***base_url*** environmental variable ie [https://cso.juniper.net](https://cso.juniper.netusername)

***username*** environmental variable, ie cso username  
***password*** environmental variable, ie cso password  
***tenant_name*** environmental variable, ie cso tenant

***site_id*** variable will be detected if ***job_id*** provided is for configure, bootstrap, zero, service provisioning

## CSO site loop
This runner will start site deployment in CSO making sure it follows correct order (configure, bootstrap, zero, service provisioning, auto-nat/sdwan/fw and dhcp update for WAN_0/1, create corresponding site in MIST if it does not exist and add SRX/vSRX to that site. Sleep for 15 minutes to gather some statistics and delete the site from CSO and MIST.

Replace or modify JSON in body of CSO-site_creation. Make sure ***site_name*** matches your selected site name if not using that variable in JSON

#### **Required**

***base_url*** environmental variable ie [https://cso.juniper.net](https://cso.juniper.net)  
***host*** environmental variable ie [https://api.mist.com](https://api.mist.com)

***username*** environmental variable, ie cso username  
***password*** environmental variable, ie cso password  
***tenant_name*** environmental variable, ie cso tenant

***site_name*** environmental variable ie PB-Abuse-vSRX

***mist_apitoken*** environmental variable ie mist api token that is valid for given organization

***org_id*** environmental variable ie mist organization ID

* * *

#### **Optional**

***site_id*** environmental variable ie mist site ID
