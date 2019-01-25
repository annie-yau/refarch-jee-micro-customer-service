FROM websphere-liberty

COPY target/CustomerOrderService-0.1.war /opt/ibm/wlp/usr/servers/defaultServer/apps/CustomerOrderService.war
COPY server.xml /opt/ibm/wlp/usr/servers/defaultServer/

RUN installUtility install --acceptLicense defaultServer

