## Description
This Repo is RTPEndpoint test program  of Kurento Media Server.  
This program cannot play RTPEndpoint RTP stream!!!!!!!!!!!!!
I am investigating how to use RTPEndpoint.  
This program make following pipline.  

PlayerEndpoint -> RTPEndpoint
               |
               -> RecorderEndpoint

If someone knows the problem, please let me know.

I want to play RTP stream from Kurento Media Server sending from RTPEndpoint.  
I attempt

## How to use
Please use the following command.  
```
  npm install
  node main --ws_uri [kurento server url]
  example) node main --ws_uri "ws://192.168.7.119:8888/kurento" --file_uri "file:///tmp/recod.webm" --video_file "file:///home/test/Desktop//output.mp4"
```
This program input input.sdp to RtpEndpointForPlayer.processOffer.
This program make output.sdp made by RtpEndpointForPlayer.processOffer.

I attempted play rtp stream using output.sdp by vlc player. 
But nothing was played.

The files sent by PlayerEndpoint are as follows.  
  http://www.gomplayer.jp/img/sample/mp4_h264_aac.mp4  
  (This is short movie. So I have linked several videos with the following command.)
  (ffmpeg -i input1.mp4 -i input2.mp4 -filter_complex "concat=n=2:v=1:a=1" output.mp4)
Recording is done. 

Why?
