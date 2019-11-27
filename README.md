# python3.7.5_ubuntu18.04
 It is a Dockerfile of slim docker image that python ver 3.7.5 runs on ubuntu 18.04

# [python of docker official image](https://hub.docker.com/_/python)

Most are based on debian , but I want a ubuntu image and it's slim.

Dockerfile is almost the same as [3.7.5-slim-buster](https://github.com/docker-library/python/blob/0b1fb9529c79ea85b8c80ff3dd85a32a935b0346/3.7/buster/slim/Dockerfile)

However, there was a part that did not work as it was. Thank you for the great experience person and correct the following two points:

1. timezone
   - Since it asks for the time zone, make sure that tzdata is entered first.
   - https://sleepless-se.net/2018/07/31/docker-build-tzdata-ubuntu/
1. gpg-server
   - Stop with "keyserver receive failed: Address not available" message
   - https://qiita.com/kakasak/items/a7898070e536db76c75b
