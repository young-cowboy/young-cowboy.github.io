title: MediaStream
speaker: 小牛仔
highlightStyle:monokai_sublime

[slide]
# MediaDevices

[slide]
## 捕获视频/音频

[slide]
长久以来，音频/视频捕获都是网络开发中的“圣杯”

（[Flash](http://www.kevinmusselman.com/2009/02/access-webcam-with-flash/) 或 [Silverlight](http://www.silverlightshow.net/items/Capturing-the-Webcam-in-Silverlight-4.aspx)）

[slide]
依靠 [WebRTC](http://dev.w3.org/2011/webrtc/editor/webrtc.html)（网络即时通信）的大力协助，寻找合适捕获 API 的步伐加快了很多。

[slide]
# WebRTC
网页实时通信（Web Real-Time Communication）谷歌2010年以6820万美元收购Global IP Solutions公司而获得的一项技术

[slide]
![](data:image/png;base64,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)

https://young-cowboy.github.io/gallery/capturing_audio_video.html

[slide]
```html
<style>
  #video{
    width: 320px;
    height: 180px;
    background-color: #000000;
  }
</style>

<video id="video" autoplay="autoplay" controls="controls"></video>

<script type="text/javascript">
  navigator
    .mediaDevices
    .getUserMedia({video: true, audio: true})
    .then(function(mediaStream) {
      var video = document.querySelector('video');

      video.srcObject = mediaStream;
      video.onloadedmetadata = function(e) {
        video.play();
      };
    })
    .catch(function(error) {
      console.log(error);
    });
</script>
```

[slide]
## MediaDevices.getUserMedia()

[slide]
允许使用一个视频和/或一个音频输入设备

[slide]
# 安全限制
## HTTPS协议 or file协议

[slide]
# 支持的约束条件
getSupportedConstraints

[slide]
```javascript
navigator
  .mediaDevices
  .getSupportedConstraints()
```

constraints 参数是一个包含了video 和 audio两个成员的
MediaStreamConstraints 对象，用于说明请求的媒体类型。

[slide]
```json
{
  "aspectRatio": true, //采集比例
  "channelCount": true,
  "deviceId": true,
  "echoCancellation": true,
  "facingMode": true,
  "frameRate": true,
  "groupId": true,
  "height": true,
  "latency": true, //延迟
  "sampleRate": true,
  "sampleSize": true,
  "volume": true,
  "width": true
  ......
```

[slide]
# 收集系统上可用的多媒体输入和输出设备的信息
## enumerateDevices

[slide]
```javascript
navigator
  .mediaDevices
  .enumerateDevices()
  .then(res => console.log(res))
```

[slide]
```json
[
  {
    "deviceId": "default",
    "kind": "audioinput",
    "label": "Default",
    "groupId": "50ec3ed5a0cff9ab1c4c5ee9aa81db10c37162fca33c03dc9b5a191dedb2e8e4"
  },
  {
    "deviceId": "e38a9b92758f008e71510a95aa36957553e2a5ce7febc6e4bcd57798807c1519",
    "kind": "audioinput",
    "label": "Built-in Microphone",
    "groupId": "50ec3ed5a0cff9ab1c4c5ee9aa81db10c37162fca33c03dc9b5a191dedb2e8e4"
  },
  {
    "deviceId": "5013c01eb0a704c09d15aa668601f8dfb80f1a33d179b2adcbb64a8fbad5fc62",
    "kind": "videoinput",
    "label": "FaceTime HD Camera",
    "groupId": ""
  },
  {
    "deviceId": "default",
    "kind": "audiooutput",
    "label": "Default",
    "groupId": "50ec3ed5a0cff9ab1c4c5ee9aa81db10c37162fca33c03dc9b5a191dedb2e8e4"
  },
  {
    "deviceId": "ba0bb7502f314e3ad61511aa6468c6a48ec679e34e5ebd975852db1d8d3ab3e7",
    "kind": "audiooutput",
    "label": "Built-in Output",
    "groupId": "50ec3ed5a0cff9ab1c4c5ee9aa81db10c37162fca33c03dc9b5a191dedb2e8e4"
  }
]
```

[slide]

## 参考资料

- [Capturing Audio & Video in HTML5](https://www.html5rocks.com/zh/tutorials/getusermedia/intro/)
- [getUserMedia](https://developer.mozilla.org/zh-CN/docs/Web/API/MediaDevices/getUserMedia)
- [enumerateDevices](https://developer.mozilla.org/zh-CN/docs/Web/API/MediaDevices/enumerateDevices)
- [getSupportedConstraints](https://developer.mozilla.org/zh-CN/docs/Web/API/MediaDevices/getSupportedConstraints)
- [MediaTrackSupportedConstraints](https://developer.mozilla.org/en-US/docs/Web/API/MediaTrackSupportedConstraints)
- [Capabilities, constraints, and settings](https://developer.mozilla.org/en-US/docs/Web/API/Media_Streams_API/Constraints#Example_Constraint_exerciser)