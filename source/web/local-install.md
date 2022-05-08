# Local Instance

To use RingTools-web on your own node, you can use the pre-made docker image, build the docker-image yourself or run the components from source.

## Umbrel using docker image

You can run ringtools-web on your umbrel node with the pre-made image:

1) Put the following in a `docker-compose.yml` file on your node:
````YAML
version: "3.7"

services:
  ringtoolsweb:
    image: ghcr.io/ringtools/ringtools-web:latest
    ports:
      - "7464:7464"
    networks:
      - umbrel
    environment:
      - PORT=7464
      - LND_REST_API_WS=wss://10.21.21.9:8080
      - LND_REST_API=https://10.21.21.9:8080
      - MACAROON_FILE=/lnd/readonly.macaroon
      - TLS_CERT_FILE=/lnd/tls.cert
    volumes:
      - /home/umbrel/umbrel/lnd/tls.cert:/lnd/tls.cert:ro
      - /home/umbrel/umbrel/lnd/data/chain/bitcoin/mainnet/readonly.macaroon:/lnd/readonly.macaroon:ro
networks:
  umbrel:
    external: true
    name: umbrel_main_network
````

2. Run it with `docker-compose up -d`
3. Your local ringtools-web instance should be available at http://umbrel.local:7464
4. To stop it, run `docker-compose stop`

If you prefer to build your own docker image, the source is available on [Github](https://github.com/ringtools/ringtools-web-docker)

## Run from source


### Server (backend)

1. Clone the server repository: `git clone https://github.com/ringtools/ringtools-server-ts`
2. Set up the `.env` tailored to your environment (see `.env.sample` for all options)
3. Install dependencies `yarn install`
4. Run the server `yarn start`
5. The backend should be available at `http://localhost:7464` (Unless you set a different value for the `PORT` environment variable)

### Frontend

1. Clone the server repository: `git clone https://github.com/ringtools/ringtools-web-v2.git`
2. If necessary, set up the `.env` tailored to your environment (see `.env.defaults` for all options) The default value works if you compile the frontend and serve it using the `server`.
3. Install dependencies `yarn install`
4. Run the server `yarn start`
5. The backend should be available at `http://localhost:4200` 

**Note**: You might need to modify the CORS settings on the server to make it work on localhost. 
