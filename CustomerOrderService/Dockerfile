FROM websphere-liberty

COPY target/CustomerOrderService-0.1.war /opt/ibm/wlp/usr/servers/defaultServer/apps/CustomerOrderService.war
COPY server.xml /opt/ibm/wlp/usr/servers/defaultServer/

RUN wget https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-5.6.3-linux-x86_64.tar.gz
RUN tar -xvf filebeat-5.6.3-linux-x86_64.tar.gz
COPY filebeat.yml /tmp/
COPY launch_container.sh /tmp
RUN chmod go-w /tmp/filebeat.yml
RUN chmod +x /tmp/launch_container.sh

RUN installUtility install --acceptLicense defaultServer

