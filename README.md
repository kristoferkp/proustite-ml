# Proustite ML

This is a repository of all the files, including my own dataset, that was used to train a football robots ML vision system. 

The video files were recorded using OBS on testing day. 

I did the labeling using Roboflow. They have excellent labeling tools. 

The training was done using Ultralytics tools which made the training super easy.

The hardest part was converting the .pt file into the .hef the Raspberry Pi AI kit expects. The AI kit uses an Hailo-8L chip.

The simplest way to convert the model is to export the model into .onnx and then use the Docker Hailo Software Suite. 

Do note that you need an x86 Linux system (preferrably Ubuntu and with a Nvidia GPU).

To download the Docker image, you need to create an account and download the files from the [Hailo Developer Zone](https://hailo.ai/developer-zone/software-downloads/?product=ai_accelerators&device=hailo_8_8l).

I would recommend to use the Raspberry Pi AI camera because the IMX500 sensor it uses has Ultralytics support, which makes the inference a lot simpler. 

The Hailo hardware is great, but the software support is lacking.