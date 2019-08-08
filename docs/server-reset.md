# Redeploy

In some special cases, the user intends to restore the VM to its original state, but it is desirable to keep all VM configuration options and associated resources reserved. At this time, we need to use the "re-deployment" operation.

1. Select the VM and select the **Redeploy** in the Support+troubleshooting section
  ![Re-deployment](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-resetstart-websoft9.png)
   
2. To confirm the action, select the Redeploy button:
  ![Confirm Reset](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetbutton-websoft9.png)

3. When the VM is ready for redeployment, the VM's Status changes to Updating, as shown in the following example:
   ![Updating](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetupdate-websoft9.png)

4. When the VM is started on a new Azure host, the Status changes to Starting, as shown in the following example:
   ![Starting](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetstarting-websoft9.png)

5. After the VM completes the boot process, the Status returns to Running, which indicates that the VM was successfully redeployed:
   ![Running](https://libs.websoft9.com/Websoft9/DocsPicture/zh/azure/azure-resetruning-websoft9.png)