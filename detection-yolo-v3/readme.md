# instruction of scripts
## setup enviornment
```
conda create -n clrnet python=3.8 -y
conda activate clrnet
conda install pytorch torchvision cudatoolkit=10.1 -c pytorch
pip install -r requirements.txt
python setup.py build develop
```
if the error: "RuntimeError: cuDNN error: CUDNN_STATUS_NOT_INITIALIZED" was shown 
```
pip install torch==1.8.0+cu111 torchvision==0.9.0+cu111 torchaudio==0.8.0 -f https://download.pytorch.org/whl/torch_stable.html
```
if the error abour cv2 occurs </br>
```
pip uninstall opencv-python
pip install opencv-python
```
## arguments
the main_script to make prediction over images captured by cameras is "cam_demo.py"</br>
run the scripts by </br>
```
python cam_demo.py configs/clrnet/clr_resnet18_video.py --validate --load_from weights/14.pth --gpus 1 --view
```
