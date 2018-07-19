# Fruit-Detector
Implementation of [TensorFlow Object Detection API on Windows 10](https://www.youtube.com/watch?v=Rgpfk6eYxJA) with fruit images without Anaconda Distribution.

# Changes

No Anaconda Distribution. Use command prompt instead of Anaconda Prompt.

1)Don't use the below commands in 2d.

```conda create -n tensorflow1 pip python=3.5```

```activate tensorflow1```

2)Change the command below in 2d

```conda install -c anaconda protobuf```

to this

```pip install protobuf --upgrade```

3)Download protoc.exe from [here](https://github.com/google/protobuf/releases/download/v3.6.0/protoc-3.6.0-win32.zip) . Copy protoc.exe(in bin folder) to C:\tensorflow1\models\research.
 
Then run 2f.

4)Before step6, open C:\tensorflow1\models\research\object_detection\utils\learning_schedules.py with a text editor.

Change the line 168 from

```range(num_boundaries)```

to

```list(range(num_boundaries))```

# Data

Data can be downloaded from [here](https://www.kaggle.com/mbkinaci/fruit-images-for-object-detection). 240 training images 60 test images. No problematic image.

3 different types of fruits: Apple, Banana, Orange.

.xml files in data have coordinates of objects.

# Training

I trained it on a GTX 1050 for 5 hours. Approximately 53000 iterations.

# Implemented Model

Faster R CNN inception v2 model.

# Youtube Video

[![TensorFlow Object Detection API](https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/my_ss.png)](https://www.youtube.com/watch?v=BCO1XdwUZYw&feature=youtu.be)

# Results on images

Input Image             |  Output Image                     
:-------------------------:|:-------------------------
<img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/trial1.jpg" width="400" height="400">  | <img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/fruit-detector1.png" width="400" height="400">  


Input Image             |  Output Image                     
:-------------------------:|:-------------------------
<img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/trial2.jpg" width="400" height="400">  | <img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/fruit-detector2.png" width="400" height="400">  


Input Image             |  Output Image                     
:-------------------------:|:-------------------------
<img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/trial3.jpg" width="400" height="400">  | <img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/fruit-detector3.png" width="400" height="400">  


Input Image             |  Output Image                     
:-------------------------:|:-------------------------
<img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/trial4.jpg" width="400" height="400">  | <img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/fruit-detector4.png" width="400" height="400">  


Input Image             |  Output Image                     
:-------------------------:|:-------------------------
<img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/trial5.jpg" width="400" height="400">  | <img src="https://github.com/MuhammedBuyukkinaci/Fruit-Detector/blob/master/images/fruit-detector5.png" width="400" height="400">  

# Credits

Credits go to [EdgeElectronics](https://github.com/EdjeElectronics). I just followed the steps in the tutorial.


