WAF - Identifying the level of protection required for applications 
===================================================================

During this lab you will use an ARM template to launch a three NIC deployment
of a cloud-focused BIG-IP VE in Microsoft Azure. Traffic flows from the BIG-IP VE
to the application servers. You will update the Azure network security group to
allow proper protocol access.

Once deployed you will work with AWAF policies to deploy the appropriate levels of protections
•	Methods of Policy Management
•	Identifying security features 
•	Building Security policies

Steps you will peform
~~~~~~~~~~~~~~~~~~~~~

#. Deploy F5 BIG-IP LTM + AWAF to new 3-NIC Azure stack
#. Launch common web attacks
#. Restore BIG-IP LTM + AWAF for lab environment
#. Work with WAF Policies

.. toctree::
   :maxdepth: 1
   :caption: Contents:
   
   deploy-azure
   attack-web
   restore-bigip
   waf-policies

