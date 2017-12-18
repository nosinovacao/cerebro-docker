# Cerebro docker image

Docker image (based on https://github.com/yannart/docker-cerebro) to run cerebro [Elasticsearch 5.x](https://www.elastic.co/products/elasticsearch) web admin tool that replaces [Kopf](https://github.com/lmenezes/elasticsearch-kopf).

Cerebro project: https://github.com/lmenezes/cerebro

This Docker image is built and available in Docker hub [nosinovacao/cerebro:latest](https://hub.docker.com/r/nosinovacao/cerebro/)

## Docker Tags

`nosinovacao/cerebro` provides multiple tagged images:

* `latest` (default): Latest version of Cerebro.
* `0.7.2`: Cerebro 0.7.2

## Usage

To run the image:
`docker run -d -p 9000:9000 --name cerebro nosinovacao/cerebro:latest`

Then you can access the web console in this URL: http://[Docker_Host]:9000

You can mount volumes for the configuration folder and / the logs, for example:

`docker run -d -p 9000:9000 --name cerebro -v /mount_folder/logs:/usr/share/cerebro/logs -v /mount_folder/conf:/usr/share/cerebro/conf nosinovacao/cerebro:latest`

Where `/mount_folder` is a folder in the Docker host to contain the data. If mounted, the volume `/usr/share/cerebro/conf` must contain a valid configuration.