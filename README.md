## gst-plugins-bad
这个版本是1.14.4的，重新编译后的srt插件供RK3568的GStreamer使用

## 改动
- gl 禁止
- srt增加了srtclientsink的streamid属性,

## srt执行语法

```shell
GST_DEBUG=3 gst-launch-1.0 -v rtspsrc location=rtsp://admin:nanchao.org@192.168.31.107:554/Streaming/Channels/101  ! rtph264depay ! h264parse ! mppvideodec ! mpph264enc  ! mpegtsmux ! srtclientsink uri=srt://192.168.0.99:10080 streamid="#\!::r=live/livestream02,m=publish"

```