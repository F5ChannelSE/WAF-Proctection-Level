WAF - Identifying the level of protection required for applications 
===================================================================

During this lab you will use an ARM template to launch a three NIC deployment
of a cloud-focused BIG-IP VE in Microsoft Azure. Traffic flows from the BIG-IP VE
to the application servers. This is the standard on-premise-like cloud design where
the BIG-IP VE instance is running with a management, front-end application traffic
(Virtual Server) and back-end application interface.

Once these devices are deployed you will learn how to create and configure
Azure Route Tables to use AFM as the gateway for desired subnets and create associated
Ingress/Egress NAT rules and policies.

Steps you will peform
~~~~~~~~~~~~~~~~~~~~~

#. Deploy F5 BIG-IP LTM + AFM to new 3-NIC Azure stack
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

