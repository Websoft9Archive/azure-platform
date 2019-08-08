# Domain Name

General techniques such as applying for a domain name and resolving domain names are not discussed in this document.

Here we introduce a more useful domain name feature of Azure: Azure provides DNS services for each virtual machine.

When the VM is configured with a dynamic IP address, the IP address may change each time the VM is restarted. As a result, the domain name needs to be re-resolved, which brings unnecessary trouble to the operation and maintenance. Azure's DNS function is to help us avoid this problem.

1. Login Azure Portal, Open the Overview of VM, Click the "Configure" of DNS name
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-opendns-websoft9.png)
2. Input your DNS name label, e.g "mysite", then Save it
   ![img](https://libs.websoft9.com/Websoft9/DocsPicture/en/azure/azure-setdns-websoft9.png)
3. Complete this setting, you can visit URL http://mysite.centralus.cloudapp.azure.com to this VM's applications