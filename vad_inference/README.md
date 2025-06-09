### Installation
Installation using the recommended versions seem outdated and does not work. Use instead:

```
conda create --name gluon python=3.7
conda activate gluon
pip install torch==1.13.1 torchvision==0.14.1 mxnet decord
pip install gluoncv --upgrade
```

### Run Inference
```
python ./scripts/action-recognition/inference.py --data-list ./vad_inference/video.txt --model i3d_resnet50_v1_kinetics400 --gpu-id -1
```

Note 1: If using GPU, remove `--gpu-id -1`
Note 2: `video.txt` contains a list of filepaths of videos to run inference on, separated by newline.
Note 3: It seems that not all models listed in the 'available models' link are available pre-trained.

Reference: https://cv.gluon.ai/build/examples_action_recognition/demo_custom.html
Available models: https://cv.gluon.ai/model_zoo/action_recognition.html, https://cv.gluon.ai/model_zoo/action_recognition.html#id187