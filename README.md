# LSB Steganography for IoT Sensor Messages

## Project Description

This project demonstrates a simple steganography technique using Python. The goal is to hide a simulated IoT sensor message inside an image using the Least Significant Bit method.

The hidden message contains example sensor information such as device ID, temperature, status, and authentication data. After embedding the message, the program extracts it again to check if the process worked correctly.

## Technologies Used

* Python
* Pillow
* NumPy
* LSB steganography
* Image processing

## How It Works

The program first converts the secret IoT message into binary. Then, each bit of the message is hidden inside the least significant bit of the image pixel values. Since only the smallest part of each pixel is changed, the visual difference between the original image and the stego image is very small.

The image is saved as PNG because PNG is lossless. This is important because formats like JPG can compress the image and destroy the hidden message.

## Example Hidden Message

```text
DEVICE_ID=Sensor_12;TEMP=27.4;STATUS=OK;AUTH=9F3A21
```

## Output Metrics

The program prints:

* Original message
* Extracted message
* Payload size
* Embedding time
* MSE
* PSNR
* Whether extraction was successful

## Why This Relates to AI and Cybersecurity

This project connects to AI and cybersecurity because steganography can be used to hide information in digital media. In cybersecurity, this can be useful for privacy and secure communication, but it can also be misused for hidden data transfer.

AI can also be used for steganalysis, which means detecting whether an image contains hidden information. This makes the topic relevant to modern security systems, where both attackers and defenders may use automated techniques.

## Conclusion

This experiment showed that a hidden IoT-style message can be embedded inside an image and extracted successfully. The visual quality remains almost unchanged, which shows why steganography can be difficult to notice without analysis tools.
