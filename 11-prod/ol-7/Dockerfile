FROM bitnami/node:11.11.0-ol-7-r4 as development

######

FROM bitnami/oraclelinux-runtimes:7-r256
LABEL maintainer "Bitnami <containers@bitnami.com>"

# Install required system packages and dependencies
RUN install_packages bzip2-libs ca-certificates glibc keyutils-libs krb5-libs libcom_err libgcc libselinux libstdc++ ncurses-libs nss-softokn-freebl openssl-libs pcre readline sqlite wget zlib

COPY --from=development /opt/bitnami/node /opt/bitnami/node

ENV BITNAMI_APP_NAME="node" \
    BITNAMI_IMAGE_VERSION="11.11.0-ol-7-r4-prod" \
    PATH="/opt/bitnami/node/bin:$PATH"

CMD [ "node" ]
