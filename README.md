# onlineBrowser
https://github.dev/github/dev

源码模式复制以下内容在dev在线终端打开

docker run -d \
  --name=chromium \
  --security-opt seccomp=unconfined `#optional` \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Etc/UTC \
  -e CHROME_CLI=https://www.google.com/ `#optional` \
  -e TITLE=sabamedia\
  -p 3000:3000 \
  -p 3001:3001 \
  -v /path/to/config:/config \
  --shm-size="1gb" \
  --restart unless-stopped \
  lscr.io/linuxserver/chromium:latest
