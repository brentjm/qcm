FROM nodered/node-red-docker:rpi

USER node-red

WORKDIR /usr/src/node-red

COPY --chown=node-red:node-red settings.js /usr/src/node-red/.
COPY --chown=node-red:node-red flows.json /data/.
COPY --chown=node-red:node-red flows_cred.json /data/.

RUN npm install node-red-dashboard \
    node-red-contrib-postgres-multi \
    node-red-node-serialport

ENTRYPOINT ["npm", "start", "--", "--useDir", "/data"]
