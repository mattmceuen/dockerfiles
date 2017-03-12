FROM quay.io/v1k0d3n/openstack-tools

MAINTAINER Matt McEuen <matt.mceuen@att.com>

# Ceph wants raw images, "qemu-img -O raw <qcow.file> <raw.file>" converts
RUN apk add --update --no-cache qemu-img \
    && rm -rf /var/cache/apk/*

COPY admin-openrc.sh /openstack-rc/admin-openrc.sh
COPY cli /bin
CMD  ["/bin/bash"]
