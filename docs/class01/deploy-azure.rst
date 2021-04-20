Deploy BIG-IP In Azure
======================

.. note:: Please note that you will incur costs associated with creating Azure resources and
   consuming F5 BIG-IP marketplace offers if you are using your own Azure account.

Launch BIG-IP 3nic stack
~~~~~~~~~~~~~~~~~~~~~~~~

#. Browse to Github to access the F5 – Azure templates

   - https://github.com/F5Networks/f5-azure-arm-templates/tree/master/experimental/standalone/3nic/new-stack/payg
   - Scroll down and click Deploy to Azure button

   .. image:: ./images/azuredeploy.png
      :scale: 40 %

#. You will be redirected to portal.azure.com

   - Log into the azure portal when prompted
   - Username : f5student#@f5custlabs.onmicrosoft.com
   - Password:  ChangeMe123

#. Complete the Customized template using the following values **(replace # with your student number to avoid conflicts)**

   +------------------------+--------------------------+
   | Resource Group         | Select Create New        |
   +------------------------+--------------------------+
   | Resource Group         | f5student#-rg            |
   +------------------------+--------------------------+
   | Location               | East US                  |
   +------------------------+--------------------------+
   | Admin Username         | azureuser                |
   +------------------------+--------------------------+
   | Admin Password         | ChangeMeNow123!          |
   +------------------------+--------------------------+
   | DNS Label              | f5student#bigip          |
   +------------------------+--------------------------+
   | Instance Name          | f5student#-f5vm01        |
   +------------------------+--------------------------+
   | Number of External IPs | 3                        |                      
   +------------------------+--------------------------+
   | Image Name             | Best25Mbps               |
   +------------------------+--------------------------+
   | BIG IP Modules         | ltm:nominal,asm:nominal  |                      
   +------------------------+--------------------------+           
   | Restricted Src Address | 0.0.0.0/0                |
   +------------------------+--------------------------+ 

   .. image:: ./images/arm3nicv2.png
      :scale: 40 %

#. Click the “Review + Create”
#. Click “Create” after confirming entries
#. This will take appoximately 10 minutes

   - You can monitor deployment on the azure dashboard by opening the Notifications in the azure portal.  Continue with the Lab. The deployment will complete by the time the BIG-IP configuration is required

#. Update Azure Network Security Group to allow required app ports

   - click on **f5student#-rg-ext-nsg** to view inbound and outbound rules

   .. image:: ./images/selectnsg.png
     :height: 350px

   - click on **inbound security rules** to view inbound rules

   .. image:: ./images/selinbound.png
     :height: 250px

   - click **Add** and fill in table on right to allow **HTTPS** then click **Add** on bottom right

   .. image:: ./images/inboundnsg.png
     :height: 250px

   - repeat steps above to allow **HTTP** and **8081**

   - final network security group should appear similar to image below

   .. image:: ./images/extnsg.png
     :height: 250px
