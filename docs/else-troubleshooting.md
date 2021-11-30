# Troubleshooting

Below are the most common problems caused by failures or setup errors.

If you have identified the problem for the reason is VM, refer to [Azure Virtual Machine Troubleshooting](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/).

#### SFTP can't connect?

Check that the account and ensure that port 22 of [Server Security Group](/network-safegroup.md) is enabled.

#### Windows Remote Desktop Connection failed?

Check that the account and ensure that port 3389 of [Server Security Group](/network-safegroup.md) is enabled.

#### The ECS not be restarted?

Please contact Azure Support Team to repair it

#### http://public IP can not open the software initialization interface?

Make sure software is installed, and the need port is enable at [Server Security Group](/network-safegroup.md)

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
