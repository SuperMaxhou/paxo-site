# Paxo site

## Build the docker image
Build everything with this command:
```sh
docker build -t ghcr.io/paxo-phone/paxo-site .
```
Then run it:
```sh
docker exec -d ghcr.io/paxo-phone/paxo-site
```
Don't forget to add all your environment variables !

## Running in a dev environment
> ℹ️ The project will consider that you have set `NODE_ENV` to `development`.

You must prepare the environement first:
```sh
yarn install
node ace migration:run
cp .env.example .env # You should edit it before launching
```

Then you can launch the website with a watchman:
```sh
yarn run dev
```

## Environment variables
|Variable name|Description|
|-------------|--------------------------------------------|
|`NODE_ENV`|Set to `developement` or `production`.|
Please complete
