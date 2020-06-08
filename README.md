# GamingVQA

Planning model can predict the gaming video quality based on the video paramters, bitrate, framerate, encoding resolution and gaming video complexity. 

In order to run the code there are two options:
- test the model based on a video information, which only the video name (and path) and complexity level ('High','Medium' ,'Low') must be specified. To do so, you can run it as follow:

-- python Planning_Model.py --video='CSGO_30fps_30sec_Part1_640x480_400_x264.mp4' --complexity='High' --test_type='test_video'

- test the model based on the video parameters, which requires specifying all video parameters, bitrate, framerate, number of pixel (width multiply height) and video complexity. E.g.:

--python Planning_Model.py --bitrate=2000 --framerate=60 --coding_res=2073600 --complexity='High' --test_type='parameters'




