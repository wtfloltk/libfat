The image `wiiulegacy/libfat` on [Docker Hub](https://hub.docker.com/r/wiiulegacy/libfat/) provides a prebuilt library in the `/artifacts` directory. Copy it into your DevkitPPC portlibs folder.  

Example:  
```
COPY --from=wiiulegacy/libfat:1.1.3a /artifacts $DEVKITPRO/portlibs
```
