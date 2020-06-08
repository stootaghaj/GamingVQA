# GamingPara: Gaming Parametric based Quality models

Planning model can predict the gaming video quality based on the video paramters, bitrate, framerate, encoding resolution and gaming video complexity. 


## How to Use
In order to run the code there are two options:
- Test the model based on a video information, which only the video name (and path) and complexity level ('High','Medium' ,'Low') must be specified. To do so, you can run it as follow:

```
    python Planning_Model.py 
        --video=CSGO_30fps_30sec_Part1_640x480_400_x264.mp4 
        --complexity=High 
        --test_type=test_video
```
- Test the model based on the video parameters, which requires specifying all video parameters, bitrate, framerate, ecoding resolution (width x height,e.g. 1920x1080) and video complexity level ('High','Medium' ,'Low').  To do so, you can run it as follow:

```
    python Planning_Model.py --bitrate=2000 
        --framerate=60 
        --coding_res=1920x1080 
        --complexity=High 
        --test_type=parameters
```

 For more help run:
 ```
    python test.py -h
```

### Application Range of Parameters 

Please note that the model only works based on the range of parameters used for training the model. 
- Bitrate: 300 kbps to 50000 kbps
- Framerate: 20 fps to 60 fps
- Resolution: 1920x1080, 1280x720 or 640×480
- Class: High, Medium, Low

### Output of the model
The model gives you four estimations: 
- Video Quality
- Video Fragementation
- Video Unclearness
- Video Discontinuity

### Example 
 ```
    sudo python Planning_Model.py 
        --bitrate=2000 --framerate=60 
        --coding_res=1920x1080 
        --complexity=High 
        --test_type=parameters
 ```
Output: 

 ```
    ('Video Quality:', 2.172123020928069)
    ('Video discontinuity:', 4.568851999906445)
    ('Video unclearness:', 1.9464660729999999)
    ('Video fragmentation:', 1.920806603456)
 ```

# Prepration 
The following steps should be performed to prepare the setup.
```
    git clone https://github.com/stootaghaj/GamingVQA.git 
    pip install -r requirements.txt
```


Install python and pip, if they are not already installed. Follow the platform specific installation instructions.
 ```
    ('Video Quality:', 2.172123020928069)
    ('Video discontinuity:', 4.568851999906445)
    ('Video unclearness:', 1.9464660729999999)
    ('Video fragmentation:', 1.920806603456)
 ```



## Citation 
Please cite the paper below if you use the code or to get more insight about the model:

@inproceedings{zadtootaghajMMSys,
  title={Quality Estimation Models for Gaming Video Streaming Services Using Perceptual Video Quality Dimensions},
  author={zadtootaghaj, Saman and Schmidt, Steven and Shafiee Sabet, Saeed and Moeller, Sebastian and Griwodz, Carsten },
  booktitle={Proceedings of the 11th International Conference on Multimedia Systems},
  year={2020},
  organization={ACM}
}
