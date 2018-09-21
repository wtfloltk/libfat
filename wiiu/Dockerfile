FROM wiiulegacy/core:0.1

MAINTAINER Maschell <maschell@gmx.de>

COPY --from=wiiulegacy/libiosuhax:0.3 /artifacts $DEVKITPRO/portlibs

RUN git clone https://github.com/Maschell/libfat && cd libfat && git checkout v1.1.3a
WORKDIR libfat

RUN make wiiu-release && \
	find $DEVKITPRO/portlibs -maxdepth 3 -type f -delete && \
	make -C wiiu install && \
	cp -r ${DEVKITPRO}/portlibs /artifacts

WORKDIR /artifacts
