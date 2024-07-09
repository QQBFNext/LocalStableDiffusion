
# On-Device Stable Diffusion

This repository showcases proof-of-concept for On-Device Stable Diffusion. In simple terms, you can create images from text using your mobile device's computational power, without needing an external server.

## Introduction

Traditional image generation from text often involves sending the text to a remote server for processing, which can result in delays due to server response times, unreliable network connections, and the limitations of server availability. it is also important to note that this approach can also raise privacy concerns. On-Device inference transforms this process by enabling your mobile device to perform the image generation locally, offering more control over what you are doing while addressing potential privacy issues.

## Models

The project incorporates the Stable Diffusion v1.4  implemented with [Keras](https://keras.io/api/keras_cv/models/stable_diffusion/). The core components of Stable Diffusion consist of three separate models: a Text Encoder, a Diffusion Model, and a Decoder Model. To make these models compatible with mobile devices, they have been converted into TFLite and ONNX formats. The resulting models are stored in the [HuggingFace repository](https://huggingface.co/anthrapper/stable_diffusion_android) for easy access.

## Application

When launching the application for the first time, it's important to note that the models, totaling around 800 MB in size, need to be downloaded. As such, users should ensure their device has enough storage space available and that a stable internet connection is accessible.

After the successful download and extraction of the models, users can proceed to input their desired prompts in the dedicated text field. Additionally, they have the flexibility to adjust both the seed value and the number of steps according to their preferences.

Throughout the process, users will have visibility into the logs, providing insight into the ongoing operations. Once the process reaches completion, the application will display the resulting image. This image can then be easily shared or saved as desired.

## Notes

- Memory Usage: To ensure smooth operation, it's best to use the app on a device with lots of free memory and with other apps closed.

- Device Heat: While uncommon, extended app usage might result in device warming. If your device feels significantly warmer, consider closing the app.

## Roadmap

- Dynamic Image Size Support ( currently the generated images are fixed to 384px resolution while Stable Diffusion 1.4 can support upto 512px resoultion )

- Full Integer Quantized Diffusion Model
- Image Inpainting
- Adding Detailed Articles on Model Creation,Quantization etc.

## License

[MIT](https://choosealicense.com/licenses/mit/)
