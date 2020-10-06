# AI / ML Sandbox
Developed by Oracle for Research

## Overview
This repository includes 
1. Base AI/ML images for creating an AI/ML sandbox instance for research
2. The images comes in two Linux operating system and hardware shapes as outlined below
3. The sandbox instances can be customized and extended for production computations

## Software & Versions
[Anaconda3-2020.07-Linux-x86_64](https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh)

## Available OS and hardware distributions 
Oracle Linux 7.8 - CPU - [URL]() - Supported with Tensor flow CPU version on all CPU shapes
Oracle Linux 7.8 - GPU - [URL]() - Supported with Tensor flow GPU version on all GPU shapes
Canonical Ubuntu 16.04 - CPU - [URL]() - Supported with Tensor flow CPU version on all CPU shapes
Canonical Ubuntu 16.04 - GPU - [URL]() - Supported with Tensor flow GPU version on all GPU shapes

## Using the image
1. Login to your Oracle cloud tenancy and navigate to Compute --> Custom Images
2. Click Import image and specify a custom image name
3. Select "Import from an object storage URL" and paste the URL of the image as shown above
4. *NOTE : It may take some time to import the image to a custom image*
5. After successful import - proceed to create the image in a supported shape
6. Select "Create Instance" and select the custom image of your choice and create the instance on your desired OCI hardware shape
7. You can use Oracle provided SSH key (download required) or put your own SSH keys to create the instance
8. SSH to the instance
  * For Oracle Linux - *SSH PrivateKey -i opc@PublicKey -L 8888:opc:8888*
  * For ubuntu - *SSH PrivateKey -i ubuntu@PublicKey -L 8888:opc:8888*
9. Start Jupyter notebook 
  * Quick start - *jupyter notebook --ip=0.0.0.0*
  * Secure start - Install a certificate for https communications from client browser
    * *openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout jupyter-key.key*
    * *jupyter notebook --certfile=jupyter-cert.pem --keyfile=jupyter-key.key*
10. Connect from browser - *http://localhost:8888*
11. Enter *notebook* as the default password to login to jupyter notebook
12. To change your password login to the instance and do *jupyter notebook password* to change your password

## Testing and benchmarking guidelines:
* NON-GPU shapes 
* GPU shapes 

## NOTES: 
1. This image is distributed with OFR Public key for troubleshooting and support. Please do not delete this from ~/.ssh/authorized_keys file

