# libtorch-yolov3
A Libtorch implementation of the YOLO v3 object detection algorithm, written with pure C++. It's fast, easy to be integrated to your production, and supports CPU and GPU computation. Enjoy ~

The code is based on the [pytorch version](https://github.com/ayooshkathuria/pytorch-yolo-v3), I rewritten it with C++.

## Requirements
1. LibTorch latest build
2. Cuda
3. OpenCV (just used in the example)


## To compile
1. cmake >= 3
2. gcc >= 5.4



```
mkdir build && cd build
cmake -DCMAKE_PREFIX_PATH="your libtorch path" ..

# if there is multi versions of gcc, then tell cmake which one your want to use, e.g.:
cmake -DCMAKE_PREFIX_PATH="your libtorch path" -DCMAKE_C_COMPILER=/usr/bin/gcc-5 -DCMAKE_CXX_COMPILER=/usr/bin/g++-5 ..
```


## Ruuning the detector

The first thing you need to do is to get the weights file for v3:

```
cd models
wget https://pjreddie.com/media/files/yolov3.weights 
```

On Single image:
```
./yolo-app ../imgs/person.jpg
```
