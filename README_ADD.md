# History to develop 

## Install modules locally

```
# remove lap from requirements.txt
pip install -r requirements.txt -f https://download.pytorch.org/whl/torch_stable.html
pip install git+https://github.com/gatagat/lap.git
python3 setup.py develop
pip install 'git+https://github.com/cocodataset/cocoapi.git#subdirectory=PythonAPI'

pip3 install cython_bbox

pip uninstall numpy
pip install numpy==1.23.3

conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia
pip install chardet

```

## Demo

```
python3 tools/demo_track.py video -f exps/example/mot/yolox_x_mix_det.py -c pretrained/bytetrack_x_mot20.tar --fp16 --fuse --save_result
```