# ao3pub-testbed

This Docker Compose project allows local testing of the ao3pub application.

## Prerequisites

You'll need [Docker](https://www.docker.com) installed on your machine. You'll
specifically need a version of Docker that supports Docker Compose. The default
Docker Desktop installation includes this.

## Setup

You should have a base directory that contains all three repositories for the
ao3pub application. This base directory can be named anything. I use the
generic `ao3pub` name for mine.

The `tweakdeveloper/ao3pub-front` repository needs to be cloned into the `front`
directory in the base directory. Similarly, the `tweakdeveloper/ao3pub-back`
repository needs to be cloned into the `back` directory within the base
directory.

After this structure is set up, the `tweakdeveloper/ao3pub-testbed` repository
can be cloned into the base directory. This directory's name doesn't matter. On
my machine, it's named `testbed`.

### Sample directory structure

```
ao3pub
├── back
├── front
└── testbed
```

## Use

When the directory structure is set up, you'll be able to enter the testbed
directory and start the Compose project:

```sh
cd testbed
docker compose up
```
