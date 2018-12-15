### Traffic Sign Detection Using YOLOv2

# Dependency 
Python 3, cython, tensorflow, numpy, opencv

# Set up 
You can use one of the following ways to do the setup.

1. Build Cython extensions
    python3 setup.py build_ext --inplace

2. Install darkflow globally in dev mode
    pip install -e .

3. Install with pip globally
    pip install .

# Change settings 
Open file "config.json" to change settings. The parameters are like the following:

{
	"yoloConfig":{
		"model": "./cfg/yolo-final.cfg", 
		"load": -1,
		"labels":"./labels.txt",
		"threshold":0.6, 
		"gpu":0.8
	}
}

Change "threshold" and "gpu" according to your situation.

# Run the program
    1. To run on a video file
    python runYOLO.py -v $filename

    2. To run on images in a folder
    python runYOLO.py -i $foldername

    3. To run on a real-time camera
    python runYOLO.py -v camera
