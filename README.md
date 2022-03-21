This runner will query site deployment in CSO making sure it follows correct order (configure, bootstrap, zero, service provisioning, auto-nat/sdwan/fw and dhcp update for WAN_0/1.

**Required**

***job_id*** environmental variable

***base_url*** environmental variable ie [https://cso.juniper.net](https://cso.juniper.netusername)

***username*** environmental variable, ie cso username  
***password*** environmental variable, ie cso password  
***tenant_name*** environmental variable, ie cso tenant

***site_id*** variable will be detected if ***job_id*** provided is for configure, bootstrap, zero, service provisioning
