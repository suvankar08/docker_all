FROM centos:7
MAINTAINER Intellipaat DevOps Batch
LABEL Vendor="CentOS" \
      License=GPLv2 \
      Version=2.4.6-40
RUN yum -y --setopt=tsflags=nodocs update && \
    yum -y --setopt=tsflags=nodocs install httpd && \
    yum clean all
EXPOSE 80
ADD run-httpd.sh /run-httpd.sh
RUN chmod -v +x /run-httpd.sh
ADD html /var/www/html
CMD ["/run-httpd.sh"]


