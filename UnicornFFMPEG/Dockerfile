FROM node:lts-alpine

ENV LB_URL=http://127.0.0.1:3001/

ENV FFMPEG_BIN_DEST=/shared

ENV FFMPEG_VERSION="2.2.1"

RUN wget https://github.com/UnicornTranscoder/UnicornFFMPEG/archive/refs/tags/$FFMPEG_VERSION.zip && unzip $FFMPEG_VERSION.zip && mv UnicornFFMPEG-$FFMPEG_VERSION UnicornFFMPEG && rm $FFMPEG_VERSION.zip

WORKDIR /UnicornFFMPEG

ADD entrypoint.sh /entrypoint.sh

ENTRYPOINT [ "/entrypoint.sh" ]