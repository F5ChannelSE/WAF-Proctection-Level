Restore BIG-IP LTM + AWAF
=========================

#. Find the public IP addresses for BIG-IP

   - click **notification icon** on top right to ensure arm deployment is complete
   .. image:: ./images/notification.png
     :height: 100px

   - search **f5student#bigip-mgmt-pip** to capture BIG-IP management public address (replace # with your student number)
   .. image:: ./images/searchbigip.png
     :height: 250px

   .. image:: ./images/bigipmgmt.png
     :height: 250px

#. Access the BIG-IP management GUI

   - browse to **https://<f5student#bigip-mgmt-pip>** (replace with ip address captured above)
   - Username: **azureuser**
   - Password: **ChangeMeNow123!**

#. Download BIG-IP archive file

   - browse to **https://github.com/F5ChannelSE/WAF-Proctection-Level/blob/main/assets/base.ucs**
   - rightclick **Download** and select **Save link as** to save base.ucs file locally

#. Upload **base.ucs** archive file to BIG-IP and restore

   - browse to BIG-IP **System->Archives** and click **upload**
   - select **Choose File** and select **base.ucs** from the location you downloaded the file then selec **Upload**
   - click **base.ucs** after uploaded
   - enter **base** for Restore Passphrase then click **Restore**.  This will take a few minutes to complete.  Click **OK** and continue to next steps.

#. Explore BIG-IP configuration

   - browse to BIG-IP **Local Traffic->Virtual Servers** to list **hackazon_vs** and **juiceshop_vs**.  (Refresh page after a few minutes before vs are listed)

   .. image:: ./images/vslistv2.png
     :height: 250px

#. Test **hackazon_vs** virtual servers

   - search for **f5student#bigip-ext-pip0** in Azure portal to capture BIG-IP Virtual Server public address
   .. image:: ./images/extpip0.png
     :height: 250px

   - browse to **http://<f5student#bigip-ext-pip0>** 
   - browse to **http://<f5student#bigip-ext-pip0>:8081** 






