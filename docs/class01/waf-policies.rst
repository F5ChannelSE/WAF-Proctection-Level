Working with WAF Policies
=========================

#. Assign waf policy to **hackazon_vs**
   
   - browse to **Local Traffic->Virtual Servers->Virtual Servers List**
   - Click the **hackazon_vs** to display Virtual Server Properties
   - Click the **Security->Policies** and ensure waf policy is selected
   - In the **Log Profile** ensure :guilabel:`waf_log` profile is selected
   - Select **update**

   .. image:: ./images/image313.png
     :height: 300px

#. Open browser and go to :guilabel:`http://<f5student#-ext-pip0>/product/view?id=101 or 1=1`.  You should receive a block message similar to below. Take note of the **Support ID** number.

   .. image:: ./images/image314.png
     :height: 70px

#. Return to hackazon main page
#. In the **Search** field type :guilabel:`<script>alert("Your system is infected! Call 999-888-7777 for help.")</script>` and press **Enter**.  You should see a similar block message. Take note of the **Support ID** number.

**Task 4 - Review WAF event logs on BIG-IP GUI.**

#. Select the **Security->Event Logs->Application->Requests** page
#. Select the :guilabel:`Event` with the matching :guilabel:`Support ID` noted on the block pages

   .. image:: ./images/image315.png
     :height: 300px


   .. NOTE::

      You can view the "Decoded Requests" and the "Original Request" however the "Response" is not captured by default.


