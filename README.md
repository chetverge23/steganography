# Steganography for IoT Sensor Messages

## Summary

This project explores how Least Significant Bit (LSB) steganography can be used to hide IoT sensor messages inside digital images. A Python implementation was developed to embed and extract hidden information while preserving the visual quality of the image. The experiment demonstrates how hidden communication can be achieved and discusses its relevance to cybersecurity and artificial intelligence.

## Background

With the rapid growth of Internet of Things (IoT) devices, security and privacy have become increasingly important. Many IoT devices continuously exchange sensitive information such as sensor readings, device identifiers, and authentication data. Traditional encryption protects the content of messages, but it does not hide the fact that communication is taking place. Steganography offers an additional layer of privacy by concealing information inside digital media such as images.

## How is it used?

In this project, a simulated IoT sensor message is hidden inside an image using the Least Significant Bit method. The message contains information such as a device identifier, temperature reading, status information, and authentication data.

Example message:

```text
DEVICE_ID=Sensor_12;TEMP=27.4;STATUS=OK;AUTH=9F3A21
```

The message is converted into binary form and embedded into the least significant bits of image pixels. After embedding, the message can be extracted from the generated stego image without noticeable visual changes to the image.

Potential applications include secure communication between IoT devices, privacy-preserving data transmission, and digital watermarking.

## Data sources and AI methods

The project uses a cover image as the data source and applies LSB steganography to hide information within the image. Python libraries such as Pillow and NumPy are used for image processing and pixel manipulation.

Although the experiment focuses on steganography rather than machine learning, it is closely related to artificial intelligence because AI techniques can be used for steganalysis. Steganalysis refers to the detection of hidden information within media files. Modern AI models can analyze patterns in images and identify modifications that may indicate hidden messages.

The experiment also evaluates image quality using metrics such as:

* Mean Squared Error (MSE)
* Peak Signal-to-Noise Ratio (PSNR)
* Embedding time
* Payload size

## Challenges

Steganography presents several challenges. If too much information is embedded into an image, visual artifacts may appear and make the hidden message easier to detect. Image compression and editing operations may also damage or destroy the hidden data.

From a security perspective, steganography can be used for legitimate privacy purposes but may also be misused to conceal malicious communications. As AI-based steganalysis techniques improve, hiding information securely becomes increasingly difficult.

## What next?

Future work could include implementing more advanced steganographic techniques, experimenting with different image formats, and integrating artificial intelligence to improve both embedding and detection methods. Other possible improvements include adaptive embedding strategies, encrypted payloads, and real-time IoT communication scenarios.

## Acknowledgments

This project was inspired by concepts studied in the Elements of AI course and by research into steganography, cybersecurity, and IoT systems. The implementation was developed using Python, Pillow, and NumPy. Additional inspiration was drawn from academic literature on steganography and AI-assisted steganalysis.
