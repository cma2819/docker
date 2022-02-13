ARG NODE_VERSION=14
FROM node:${NODE_VERSION}

RUN mkdir /nodecg
WORKDIR /nodecg

RUN npm install -g nodecg-cli && \
    nodecg setup

ARG DEPENDENCY_BUNDLES
RUN for BUNDLE in ${DEPENDENCY_BUNDLES}; do \
    nodecg install ${BUNDLE}; \
    done;

VOLUME [ "/nodecg/bundles", "/nodecg/cfg", "/nodecg/db", "/nodecg/logs" ]
EXPOSE 9090

CMD ["nodecg", "start"]