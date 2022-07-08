FROM zabbix/zabbix-server-pgsql:ubuntu-5.4.8

USER root

# Update Software repository
RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y dnsutils

RUN wget http://pastebin.com/raw.php?i=p3QyuXzZ -O /usr/share/snmp/mibs/ietf/SNMPv2-PDU

EXPOSE 10051/TCP

USER 1997

CMD ["/usr/sbin/zabbix_server", "--foreground", "-c", "/etc/zabbix/zabbix_server.conf"]
