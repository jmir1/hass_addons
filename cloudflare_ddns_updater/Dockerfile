ARG BUILD_FROM
FROM $BUILD_FROM

# Install ddclient
RUN apk add ddclient && apk add jq && apk add iproute2

COPY ddclient.conf /etc/ddclient/ddclient.conf

# Copy data for add-on
COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]