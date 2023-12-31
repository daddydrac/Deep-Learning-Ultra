# Deep Learning Ultra
Open source Deep Learning Containers (DLCs) are a set of Docker images for training and serving models with MLFlow in PyTorch, OpenCV (compiled for GPU), TensorFlow 2 for GPU, PyG and NVIDIA RAPIDS, running on CUDA 12.1. Tensorboard included for visualizations into model explainability and fine-tuning/understanding how your model learns.

### Used and adopted by many!

| ![Open source Deep Learning Containers (DLCs) ](./misc/h20ai.png) | ![Open source Deep Learning Containers (DLCs) ](./misc/nasa.png)    | ![Open source Deep Learning Containers (DLCs) ](./misc/tcs.png)    |
| :---:   | :---: | :---: |
| ![Open source Deep Learning Containers (DLCs) ](./misc/220px-Argo_AI_logo.svg.png) | ![Open source Deep Learning Containers (DLCs) ](./misc/argonne-logo-1200x1000.png)   |![Open source Deep Learning Containers (DLCs) ](./misc/HPE_Cray_678x452.png)   |
| ![Open source Deep Learning Containers (DLCs) ](./misc/army_ai_task_force.png) | ![Open source Deep Learning Containers (DLCs) ](./misc/cisco.png)   |![Open source Deep Learning Containers (DLCs) ](./misc/deloitte.png)   |


### Ultra easy deployment

Edit [line 18](https://github.com/daddydrac/Deep-Learning-Ultra/blob/main/docker-compose.yml#L18) in docker-compose.yaml for however many GPUs you have: ```count: 3  # num of gpus```, then run:

```docker compose up --build -d```

   - Get security token to log into the notebook:

     ```
     token=$(docker exec -it ultra /bin/bash -c "jupyter notebook list") \
     echo ${token::-8}
     ```


### Requirements
 - Linux configured with ```nvidia-container-toolkit``` [found here](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html), CUDA 12, NVIDIA Drivers v.525+
 - NVIDIA GPU ```-ARCH_7.5+```


## Deep Learning Container Services

1. Deep Learning Notebook, or you can mount VSCode to ```/app``` | [http://localhost:8888](http://localhost:8888)
2. MLFlow is an open source platform for managing the end-to-end machine learning lifecycle, see more [here](https://mlflow.org/docs/latest/what-is-mlflow.html) 
 | [http://localhost:5000](http://localhost:5000)
3. Tensorboard povides the visualization and tooling needed for machine learning experimentation | [http://localhost:6006](http://localhost:6006)

 - <strong>Deep learning solution</strong>  - all python bindings specifically compiled for c++/CUDA:
   - Pytorch 2
   - PyG (Graph Neural Networks)
   - NVIDIA RAPIDS
   - OpenCV v4.8
   - TensorFlow 2
    
 - CuPy, Anaconda Python v3.11.5, Captum, MLFlow and more!
   
 - Supports LLMs, HuggingFace, Computer Vision, Navigation, Physics Informed ML, and Graph Neural Networks

----------------------------------------------------------------------------

![a](./misc/b.png)
![a](./misc/d.png)
