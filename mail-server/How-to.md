# How-to

---

## Build the docker image

Edit Dockerfile
Update line

> ./run.py --force localhost

with your mail domain eg..

> ./run.py --force example.com

This will produce a server on

> mail.example.com

Build the the image
tag with organation / image name then the version eg ..

> docker build -t acme/mail-server:1.0 .

My looks like this

> docker build -t ryunet/mail-server:master .

**note the dot at the end**
