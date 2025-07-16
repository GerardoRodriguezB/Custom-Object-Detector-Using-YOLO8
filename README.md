# Custom-Object-Detector-Using-YOLO8
In this repository I explain step by step how to create an anaconda environment with the versions o packages necessary to train a custom object detection using YOLO 8


First we create the anaconda environment with python 3.10

```bash
conda create -n env_name python=3.10
```

Then we activate to the environment we created 

<pre>```bash
conda activate env_name
```</pre>

xd

<pre> ```bash conda create -n env_name python=3.10 conda activate env_name ``` </pre>

We install specific versions of some packages to avoid compatibility problems

```bash
pip install ultralytics==8.0.114 pandas==2.0.2 opencv-python==4.7.0.72 numpy==1.24.3 scipy==1.10.1 easyocr==1.7.0 filterpy==1.4.5
```


