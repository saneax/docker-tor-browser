# docker-tor-browser
a tor browser on docker container, which can play sound

docker run -t -i --rm -v $XDG_RUNTIME_DIR/pulse:$XDG_RUNTIME_DIR/pulse \
-v /media/crypto/sanjayu/:/home/user/tor-browser-data/ \
-v /tmp/.X11-unix:/tmp/.X11-unix \
-v /dev/shm:/dev/shm \
-e DISPLAY=unix$DISPLAY \
-e PULSE_SERVER=unix:$XDG_RUNTIME_DIR/pulse/native \
ifirefox:latest

/media/crypto/sanjayu/ is a luksFormat disk, could be in your pen drive as
well, so that should keep your downloads, or uploads secret too.
