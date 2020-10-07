# Video Editor

Video editing tool using ffmpeg.
The tool has the ability to cut as many unnecessary video frames as specified in a YAML file.

## Dependencies
- ffmpeg

## Install
Use ```pip install -i https://test.pypi.org/simple/ video-editor``` to install.

## Create a YAML with the frames to cut or select
. Sample YAML ```myrecording.yaml```
```
---
input: "input-video.mp4"
output: "output-video.mp4"
cut_method: select  # use delete to delete the frames
timeframe:
  - from: start   # first frame
    to: 4m
  - from: 10m11s  # unwanted frames
    to: 15m50s
  - from: 30m5s   # unwanted frames
    to: end       # last frame
```
. Execute
```video-cut -p myrecording.yaml```

. You should now get the ```output-video.mp4``` after the process is over.

## Future enhancements
- Move from ```ffmpeg``` tool to ```ffmpeg-python``` library
- Add feature to screen grab based on screen coordinates 
