# Troubleshooting

Below are the most common problems caused by failures or setup errors.

If you have already identified the cause of the problem as a VM, please read [Azure Virtual Machine Troubleshooting](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/).

#### SFTP can't connect?

Check that the account number and password are correct. Please ensure that port 22 of [Server Security Group](/network-safegroup.md) is enabled.

#### Windows Remote Desktop Connection failed?

Check that the account number and password are correct. Please ensure that port 3389 of [Server Security Group](/network-safegroup.md) is enabled.

#### The VM not be restarted?

Please contact Azure to repair it

#### Http://public IP can not open the software initialization interface?

Check if the required software is installed, please ensure that port 80 of [Server Security Group](/network-safegroup.md) is enabled.

#### Can't create VM from your image which from Marketplace?

We know using image or VHD to create VM is a reasonable operation for user on Azure Portal. But the Azure have a "issue" when image is from Marketplace for creating VM. If you delete your Wordpress VM and only retain the VHD, then create VM from VHD, you can also get the similar error.

Why this error?  I think when creating VM from your image, azure system will verify the subscription information of image, but azure portal have no selection for this

How to sovle this?

1. Use Azure Powershell to get your image subscription plan of Marketplace
```
PS Azure:\> az vm image list --offer w9wordpress2 --all --output table
Offer         Publisher    Sku                          Urn                                                             Version
------------  -----------  ---------------------------  --------------------------------------------------------------  ---------
w9wordpress2  websoft9inc  wordpress52-lemp72-centos76  websoft9inc:w9wordpress2:wordpress52-lemp72-centos76:5.2.20000  5.2.20000
```

2. Create VM from your image, at the last step please download this template
https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-dltemplate-websoft9.png

3. Find the "resources" [  "properties[]" ]  item in the template, add the follow plan to properties[]
```
"plan": {
                "name": "wordpress52-lemp72-centos76",
                "publisher": "websoft9inc",
                "product": "w9wordpress2"}
```
4. Save the template
5. Click "Deploy"