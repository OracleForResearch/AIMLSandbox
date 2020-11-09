# Research Image Sandbox
Developed by Oracle for Research

## Goal 
Provide researcher with 
1. A sandbox environment to get researhers quickly up and running.
2. Researcher may need separate CPU and GPU images

## Overview
This repository includes 
1. Images that can be quickly imported by researchers.
2. Images are developed and supported by Oracle for Research
3. Images should be pulled down as a URL and imported as a custom image in your tenancy before usage

## Software & Versions
2. [Included software versions](https://github.com/OracleForResearch/AIMLSandbox/blob/main/SoftwareAndVersion)

## Downloads
Distributed from Oracle for Research object store
#### AI/ML Sandbox 
1. [AI/ML Sandbox-OL7.8-CPU](https://github.com/OracleForResearch/AIMLSandbox/blob/main/images/MLSandboxTFCPU-OL78) - Supported with Tensor flow CPU version on all CPU shapes
2. [AI/ML Sandbox-OL7.8-GPU](https://github.com/OracleForResearch/AIMLSandbox/blob/main/images/MLSandboxTFGPU-OL78) - Supported with Tensor flow GPU version on all GPU shapes
3. [AI/ML Sandbox-Ubuntu16.04-CPU](https://github.com/OracleForResearch/AIMLSandbox/blob/main/images/MLSandboxTFCPU-Ubuntu18.04) - Supported with Tensor flow CPU version on all CPU shapes
4. [AI/ML Sandbox-Ubuntu16.04-GPU](https://github.com/OracleForResearch/AIMLSandbox/blob/main/images/MLSandboxTFGPU-Ubuntu18.04) - Supported with Tensor flow GPU version on all GPU shapes
#### Afni Sandbox
1. [Afni-Ubuntu-20.04v1](https://objectstorage.us-ashburn-1.oraclecloud.com/p/Umjj9GfKkP3_vRvEDbc7wsh47MQAxwOdNh5C-If82m46vDXC1D3-0lDvLCVe4TGY/n/ideqbfsd51fu/b/OFRImages/o/AFNI-Ubuntu-20.04-v1)
#### Research Gateway 
1. [Research Gateway OCI CLI](https://objectstorage.us-ashburn-1.oraclecloud.com/p/98pDM54dEywfQvlbS0HVbeeKSbYuLIUUjoi6yYCkqEakA2rhdeXbEzPV2ReU8Y6k/n/ideqbfsd51fu/b/OFRImages/o/Research-Gateway) - A research gateway image pre-installed with OCI CLI. It is recommended to use a free tier VM in a public subnet to host this VM

## Using the AI/ML Sandbox image
1. Login to your Oracle cloud tenancy and navigate to Compute --> Custom Images
2. Click Import image and specify a custom image name
3. Select "Import from an object storage URL" and paste the URL of the image as shown above
4. *NOTE : It may take some time to import the image to a custom image*
5. After successful import - proceed to create the image in a supported shape
6. Select "Create Instance" and select the custom image of your choice and create the instance on your desired OCI hardware shape
7. You can use Oracle provided SSH key (download required) or put your own SSH keys to create the instance
8. SSH to the instance
  * For Oracle Linux - *SSH -i PrivateKey -i opc@PublicIP -L 8888:localhost:8888*
  * For ubuntu - *SSH -i PrivateKey ubuntu@PublicIP -L 8888:localhost:8888*
9. Start Jupyter notebook 
  * Quick start - *jupyter notebook --ip=0.0.0.0*
  * Secure start - Install a certificate for https communications from client browser
    * *openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout jupyter-key.key*
    * *jupyter notebook --certfile=jupyter-cert.pem --keyfile=jupyter-key.key*
10. Connect from browser - *http://localhost:8888*
11. Enter *notebook* as the default password to login to jupyter notebook
12. To change your password login to the instance and do *jupyter notebook password* to change your password

## Hardware shape support:
* All OCI CPU shapes 
* All OCI GPU shapes 

## Requsting OFR Technology assistance: 
1. Please add the OFR SSH public key to ~/.ssh/authorized_keys file in your running instance/boot volume before requesting assistance
2. This is only required for OFR Technology team to login into your instance

## References
1. [Anaconda3-2020.07-Linux-x86_64](https://repo.anaconda.com/archive/Anaconda3-2020.07-Linux-x86_64.sh) 
2. [AFNI](https://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/steps_linux_ubuntu18.html)

