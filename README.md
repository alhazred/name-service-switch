# name-service-switch
Simple name-service-switch SMF service for illumos

Usage: 
     
     
      $ svccfg import /lib/svc/manifest/system/name-service-switch.xml
      $ svccfg -s name-service-switch setprop config/default = false
      $ svccfg -s name-service-switch setprop config/hosts = astring: \"files dns mdns ldap\"
      $ svccfg -s name-service-switch:default refresh
      
Setting /etc/nsswitch.conf to default (nsswitch.dns):


      $ svccfg -s name-service-switch setprop config/default = true
      $ svccfg -s name-service-switch:default refresh
      
