title: MediaStream
speaker: 影逸

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

## MediaDevices.getUserMedia()

[slide]

允许使用一个视频和/或一个音频输入设备

[slide]

## demo

[【capturing_audio_video】](https://young-cowboy.github.io/gallery/capturing_audio_video.html)

[slide]

## HTTPS协议 or file协议

[slide]

## constraints

[slide]

getSupportedConstraints

[slide]

```javascript
navigator
  .mediaDevices
  .getSupportedConstraints()
```

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
}
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