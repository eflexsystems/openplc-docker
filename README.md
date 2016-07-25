# openplc-docker
Docker containers for openplc server and editor

#### To run on docker for mac
1. Install [XQuartz](https://www.xquartz.org/)
2. Run `socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\"` in a separate terminal
3. `docker run  -e DISPLAY=your-ip-here:0 eflex/openplc-editor`

