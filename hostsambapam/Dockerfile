# Version: 0.0.1
# Aitor Galilea@edt M06 2018-2019
# cliente SAMBA capaz de automontar directorios mediante PAM
# -----------------------------------------------------------
FROM fedora:27
LABEL author="Aitor Galilea@edt ASIX M06-ASO"
LABEL description="host PAM 2018-2019"
RUN dnf -y install procps vim less nmap iproute passwd openldap-clients nss-pam-ldapd authconfig pam_mount cifs-utils samba-client
RUN mkdir /opt/docker
COPY * /opt/docker/
RUN chmod +x /opt/docker/install.sh /opt/docker/startup.sh /opt/docker/authconfig.conf
WORKDIR /opt/docker
CMD ["/opt/docker/startup.sh"]
