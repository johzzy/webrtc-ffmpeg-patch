WebRTC FFmpeg Patch
-------------------

Android WebRTC 开启 FFmpeg 解码和 OpenH264 编码

# ffmpeg commit in .gclient_entries

`  'src/third_party/ffmpeg': 'https://chromium.googlesource.com/chromium/third_party/ffmpeg.git@6d9096c9e3f7f5d4e6528104ed77987ec9327315',`

# create patch

```
cd src/third_party/ffmpeg
git diff > /tmp/ffmpeg.patch
```

# apply patch
```
cd /tmp
git clone https://github.com/johzzy/webrtc-ffmpeg-patch
git apply --stat   /tmp/webrtc-ffmpeg-patch/patch/ffmpeg.patch
git apply --check /tmp/webrtc-ffmpeg-patch/patch/ffmpeg.patch
git am --signoff < /tmp/webrtc-ffmpeg-patch/patch/ffmpeg.patch

```
