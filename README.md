# Mongo tutorial for ALeRCE

Tutorial for (py)mongo, geared towards ALeRCE users.

## Set up

To install all dependencies needed for this tutorial run,

```bash
pip install -r requirements.txt
```

To set up the database we'll be using during the tutorial, you'll need
to [install docker compose](https://docs.docker.com/compose/install/).

To run the container, use:

```bash
docker compose up -d
```

**Note:** If you have an old version of docker compose, the above command
might need to be replaced by:

```bash
docker-compose up -d
```

This will create a Docker container with MongoDB running in it, as per the instructions in
the `docker-compose.yml` file provided here. The `-d` flag allows for it to run in the
background.

To stop the container, run:

```bash
docker compose down
```

As above, depending on your version, you might need to use `docker-compose` instead of
`docker compose`.

## Loading data

There are scripts that will load data into the database (used from module 2
onwards). To insert all the data run the following (while the docker container is running):

```bash
python scripts/populate.py
```

## Start the tutorial

To start the tutorial, run:

```bash
jupyter-lab
```

A browser tab should be opened and from there you can navigate to the `tutorial` folder, where
the notebooks are sorted from first to last module.