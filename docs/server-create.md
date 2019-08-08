# Create

Here's how to create a VM on Azure.

The most basic condition for creating a virtual machine is to prepare a boot disk file for the system disk for the virtual machine. There are two types of template files: one is a image that we are very familiar with, and the other is a VHD (virtual disk) file.

Therefore, there are two ways to create a VM: image-based creation and system-based disk creation.

## Image-based Creation

1. Log in to the Azure Portal and open: VM -> Create a virtual machine

2. Select the appropriate image when creating the VM (this is the most important step)
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-createvmbyimage-websoft9.png)

> Image sources are: official image, Marketplace image and Customized image. If you use the customized image source, the disk can only choose the hosting mode.

3. Set the account password, network, security group, etc.

4. "Review + create" after you pass, click "Next"

## VHD Creation

1. Log in Azure Portal, click "All Resources", find a disk that has been unattached
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-createvmbydisk-websoft9.png)
2. Click the "Create VM"
3. Set the account password, network, security group, etc.
4. "Review + create" after you pass, click "Next"

## SSH Key

When creating a VM, some users prefer to use the SSH key pair as the login credentials.
   ![image.png](http://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-createvmsshkey-websoft9.png)

Since Azure needs to provide its own SSH public key, it requires the user to prepare in advance.

Take PUTTYGEN (KEY GENERATOR FOR PUTTY ON WINDOWS) as an example to illustrate how to create an SSH public key.

1. Download and Install [PUTTYGEN](https://www.ssh.com/ssh/putty/windows/puttygen).

2. Click "Generate"  
   ![image.png](https://libs.websoft9.com/Websoft9/DocsPicture/en/putty/puttygen-generate-websoft9.png)

3. Public key and Private key is OK, you can copy public to Azure(format starting with "ssh-rsa") ,and Save the public key and private key on your local computer for backups
   ![image.png](https://libs.websoft9.com/Websoft9/DocsPicture/en/putty/puttygen-generatesave-websoft9.png)

4. When connect Linux on your local computer, you can use private key for authentication 


