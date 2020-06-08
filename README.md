# GamingVQA

Planning model can predict the gaming video quality based on the video paramters, bitrate, framerate, encoding resolution and gaming video complexity. 

In order to run the code there are two options:
- test the model based on a video information, which only the video name (and path) and complexity level ('High','Medium' ,'Low') must be specified. To do so, you can run it as follow:

```
    python Planning_Model.py --video=CSGO_30fps_30sec_Part1_640x480_400_x264.mp4 --complexity=High --test_type=test_video
```
- test the model based on the video parameters, which requires specifying all video parameters, bitrate, framerate, ecoding resolution (width x height,e.g. 1920x1080) and video complexity level ('High','Medium' ,'Low').  To do so, you can run it as follow:

```
    python Planning_Model.py --bitrate=2000 --framerate=60 --coding_res=1920x1080 --complexity=High --test_type=parameters
```



