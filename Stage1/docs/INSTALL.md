## Installation
- install the virtual environment and pytorch:
  ```
  conda create --name ev3d_stage1 python=3.10
  conda activate ev3d_stage1
  pip install torch==2.14.1 torchvision==0.29.1
  # pip install torch==1.10.0+cu111 torchvision==0.11.0+cu111 torchaudio==0.10.0 -f https://download.pytorch.org/whl/torch_stable.html
  ```

- install cmake:
  ```
  conda install cmake
  ```

- install sparse conv:
  ```
  pip install spconv-cu126
  ```

- install Waymo evaluation module:
  ```
  # pip install waymo-open-dataset-tf-2-0-0
  ```

- install the requirements of LoGoNet:
  ```
  pip install -r requirements.txt
  ```

### The following procedures can be performed via bash commands
```
bash setup_py.sh
```

- install the requirements of image_modules:
  ```
  cd detection/al3d_det/models/image_modules/swin_model
  pip install -r requirements.txt
  pip install -e . --no-build-isolation
  cd -
  ```

- compile LoGoNet:
  ```
  cd utils
  pip install -e . --no-build-isolation
  cd -
  ```
- compile the specific algorithm module:
  ```
  cd detection
  pip install -e . --no-build-isolation
  cd -
  ```
- compile the specific dcn module:
  ```
  cd detection/al3d_det/models/ops
  pip install -e . --no-build-isolation
  cd -
  ```