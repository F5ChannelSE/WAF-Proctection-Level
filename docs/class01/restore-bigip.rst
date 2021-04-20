Restore BIG-IP LTM + AWAF
=========================

#. Find the public IP addresses for BIG-IP

   - browse to Azure portal and select your **f5student#-rg**
   - search **f5student#bigip-mgmt-pip** to capture BIG-IP management public address
   - search **f5student#-ext-pip0** to capture BIG-IP Virtual Server public address


#. Access the BIG-IP management GUI

   - browse to **https://<f5student#bigip-mgmt-pip>** (replace with ip address captured above)
   - Username: **azureuser**
   - Password: **ChangeMeNow123!**

#. Download BIG-IP archive file

   - browse to **https://github.com/F5ChannelSE/WAF-Proctection-Level/blob/main/assets/base.ucs**
   - click **Download** to save base.ucs file locally

#. Upload **wafbase.ucs** archive file to BIG-IP and restore

   - browse to BIG-IP **system->archives** and click **upload**
   - select **Choose File** and select **wafbase.ucs** from the location you downloaded the file
   - click **wafbase.ucs** after uploaded
   - enter **base** for Restore Passphrase then click **Restore**.  This will take a few minutes to complete.

#. Explore BIG-IP configuration

   - browse to BIG-IP **Local Traffic->Virtual Servers** to list **hackazon_vs** and **juiceshop_vs**

   .. image:: ./images/vslist.png
     :height: 250px

   - browse to BIG-IP **Security->Application Security** to list the waf policies restored

   .. image:: ./images/waflist.png
     :height: 250px

#. Test **hackazon_vs** virtual servers

  - browse to **https://<f5student#-ext-pip0>** 
  - browse to **http://<f5student#-ext-pip0>:8081** 






