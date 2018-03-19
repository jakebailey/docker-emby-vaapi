# docker-emby-vaapi

This Docker image is based on dperson/emby, but instead downloads Debian's
ffmpeg build and vaapi drivers for HW encoding support. Mount `/dev/dri` into
the container to give emby access.

This image depends on knowing the host system's groupid for the user who owns
`/dev/dri`, which on Arch Linux is 91. Set the `VIDEO_GID` build arg to
override.
