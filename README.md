# Focalboard arm64 container workflow

this is just a simple Github workflow that clones the [mattermost/focalboard](https://github.com/mattermost/focalboard) repository and builds it with multiple platforms, which is possible, according to their [docker/README.md](https://github.com/mattermost/focalboard/blob/main/docker/README.md).

Currently the workflow builds only the linux/arm64 platform as other arm platforms (tested with arm/v7 and arm/v8) are not possible due to a dependency on Cypress (a `npm` package) which only supports x86_64 and arm64.

## Motivation

Quite simple: I wanted to run Focalboard on my Raspberry Pi with a 64 Bit OS at home, but there is no official pre-built Focalboard arm64 image, even though the Dockerfile supports it since their [Pull request #1700](https://github.com/mattermost/focalboard/pull/1700) was merged.

Also, I wanted to learn a bit of how Github workflows work and this seemed like a good first mini-project.

## Testing
~~As of now (2023-10-17), the image has not yet been tested. I will try to run it on arm64 but~~ I tested the image on my Raspberry Pi 4 and it seems to work fine. I still probably won't be able to test it thoroughly.

For more in depth tests it would be much appreciated if anyone wants to test it and report on their findings.

Alternatively if anyone wants to help set up automated testing (no experience on that yet on my part), that would be nice as well. 
