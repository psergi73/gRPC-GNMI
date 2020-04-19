# gRPC-GNMI
This repository contains a Java GNMI Client. 

Download the zip file  locally and issue the below command  from the  root folder. Depending  if i t  will run ona Windows or Linux machine  the syntax is slightly different.

JRE 1.8 is a prerequisite to run the application


Linux:  java  -cp .;./com/grpc/gnmi/client/lib/*  com.grpc.gnmi.client.GNMIMain  --interval  <it is in seconds, minimum 10 seconds> --encoding JSON --username <username> --password  <password>  --serverip  <ip address> --serverport  57400 --mode <STREAM or ONCE>  --resource  <XML Path>  i.e /state/port[port-id=1/1/6]/ethernet/statistics/total-octets or  /state/service/vpls[service-name=*]/sap[sap-id=*]/egress/qos/sap-egress/traffic-manager/stat

Windows:  -cp .;.\com\grpc\gnmi\client\lib\*  com.grpc.gnmi.client.GNMIMain  --interval  <it is in seconds, minimum 10 seconds> --encoding JSON --username <username> --password  <password>  --serverip  <ip address> --serverport  57400 --mode <STREAM or ONCE>  --resource  <XML Path>  i.e /state/port[port-id=1/1/6]/ethernet/statistics/total-octets or  /state/service/vpls[service-name=*]/sap[sap-id=*]/egress/qos/sap-egress/traffic-manager/stat

Presently the application works only in unsecure mode (without TLS)  and the timeout is hardcoded   to 5 * interval time . 
The application has been tested and validated with Nokia 7750 SR routers.
