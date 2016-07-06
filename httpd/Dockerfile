FROM parana/systemd_rawhide
RUN yum -y install httpd; yum clean all; systemctl enable httpd.service
EXPOSE 80

# We need create this directory otherwise Apache doesn't start 
RUN mkdir -p /var/log/httpd
# RUN chmod 777 /var && chmod 777 /var/log && chmod 777 /var/log/httpd && chmod 777 /etc && chmod 777 /etc/httpd 
# To verify the symlink
RUN ls -lat /etc/httpd && ls -lat /var/log

CMD [ "/usr/sbin/init" ]

