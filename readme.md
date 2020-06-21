# What's this?

Docker image w all FFMPEG dependecies compiled for streaming via RTMP.
Inspired by this post: [[Compile FFmpeg with RTMPS for Facebook](http://www.iiwnz.com/compile-ffmpeg-with-rtmps-for-facebook/)]


# Run on Docker:

Set the path to the video file you want to stream and the path to the RTMP server or optionally overrite the whole runtime [command](https://docs.docker.com/engine/reference/commandline/run/#usage)

```bash
# PATH_TO_VIDEO_FILE= #TODO
# FACEBOOK_URL_RTMPS='rtmps://live-api-s.facebook.com:443/rtmp/...' #TODO

docker run \
    --rm \
    -e URL_RTMPS=$FACEBOOK_URL_RTMPS \
    -v $PATH_TO_VIDEO_FILE:/usr/app/input.mp4 \
    docker.pkg.github.com/yoga1290/ffmpeg2rtmp/ffmpeg2rtmp:20.06.0
    #[COMMAND] [ARG...]
```
