

# Impulse Classification Network (ICN) for video Head Impulse Test

This research proposes the Impulse Classification Network (ICN) using 1D Convolutional Neural Network (1D CNN) that able to detect noisy data and classify human VOR impulses. ICN is a high-performance classification method that works on a patient's video Head Impulse Test (vHIT) impulse data by identifying abnormalities and artifacts. Our ICN method found actual classes of patient’s impulses with 95% accuracy. 


We provide train and test python files. We created our dataset which came from the ICS goggle device.


Lateral canal test type: left side vHIT data with a) normal and b) artifact impulses

- [x] 
![normal_impulses](/images/normal_impulses.png)

- [x]
![artifacts](/images/artifact_impulses.png) 


#### Type of classes

1) Normal - 1081,
2) Abnormal -	804,
3) Artifact_phase_shift - 797,
4) Artifact_high_gain - 1115

Total	**3797** impulses



### Training part
--------------

 ```bash 
 python train.py -l labels.pickle
```

### Test part
----------

``` bash
python test.py -m ./data/yourmodel.h5 -l lables.pickle -i impulse.csv
```

### Result 
![](/images/classification.PNG)

We can check the VOR gain values and predict the class of each impulse. 

Artifact_high_gain – 100%
![](/images/Figure_131.png) 
Normal class is detected 93.44%
![](/images/Figure_181.png) 
Artifact_phase_shift – 98.72%
![](/images/Figure_211.png)



Dataset will be uploaded soon!!!
