# jinkies-composed
dockerfiles to compose a jinkies

## setup

Download jenkins long term service war.
```bash
OUTPUT_PATH=/path/to/jinkies-composed/build_zone jenkins-prep-scripts/bin/downloadjenkins
```

From `/path/to/jinkies-composed/build_zone`, run the instance with
```bash
./build_image
docker run playtechnique/jikies:latest
```

At this point it is an unconfigured instance.
