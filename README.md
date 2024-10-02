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

## Starting the testbed

When the directory structure is set up, you'll be able to enter the testbed
directory and start the Compose project:

```sh
cd testbed
docker compose up
```

## Accessing the testbed

Through the magic of nginx, the frontend's files live in the `/` HTTP path and
the backend's routes live in the `/api` path.

### Testing the frontend

You'll be able to test frontend functionality by navigating to
`http://localhost:8080` in your preferred browser.

### Testing the backend

Similarly, you'll be able to access backend functionality by prefixing the route
with `http://localhost:8080/api`. For example, the API route
`/work/<work_id>/metadata` becomes
`http://localhost:8080/api/work/<work_id>/metadata`. This can be tested with
your favorite HTTP client (curl, Postman, etc.)
