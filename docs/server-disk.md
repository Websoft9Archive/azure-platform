# Disk

For the Azure, a disk can be a separate computing resource (created separately, billed separately, managed separately, etc.) and can be integrated into a VM as a component.

There are several special concepts in Azure's disk management, explained in advance:

* Managed Disk: Hosted by Azure Public Store
* Unmanaged disk: The disk can only be managed by the storage account under the account, not as an independent resource.
* Storage account: Azure provides a storage account function, the so-called storage account, which is an entry that can manage the disk.

## Data Disk

We know that a data disk is different from the system disk and is mainly used to store data.

### Add Data Disk

1. Login Azure Portal, select the VM and Stop it
2. Open the Setting->Disks of Stopped VM, click the button "Add data disk"
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-addddisk-websoft9.png)
3. Set the disk name,size and other information
   ![setting datadisk](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-addddisk2-websoft9.png)
4. Connect to OS to initialize disk
    - Windows, please refer to Azure official documantation [Initialize Windows disk](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/attach-managed-disk-portal#initialize-a-new-data-disk)
    - Linux, please refer to Azure official documantation [Initialize Linux disk](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/attach-disk-portal#connect-to-the-linux-vm-to-mount-the-new-disk)
5. Finish adding data disk

### Detach Data Disk

1. Login Azure Portal, select the VM and Stop it
3. Open the Setting->Disks of Stopped VM
4. Click the "Edit" on the top of Disks page
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-ddiskds-websoft9.png)
5. Then, click the detach icon like below
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-ddiskds2-websoft9.png)
6. Once detach disk, please save it
7. Start VM

> The disk detach didn't deleted, it remain in the storage account

## Change Size

You can change the Size or change the Account type of Data Disk when the disk is not mounted to VM

![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-ddiskin-websoft9.png)

> In most times, the disk can only increase size, not reduce size.