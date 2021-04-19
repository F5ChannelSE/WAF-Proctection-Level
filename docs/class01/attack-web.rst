Launch Common Web Attacks
=========================

#. Open browser and go to :guilabel:`https://52.186.95.146/` to access the unprotected **Hackazon** website
#. Under **Special selection** click on any sale item displayed
#. Note the **product id** in the browser address bar

   .. image:: ./images/image392.png
     :height: 400px

#. In the browser address bar append :guilabel:`or 1=1` then press **Enter**

   .. image:: ./images/image393.png
     :height: 50px

   .. NOTE::

      This is a common :guilabel:`sql injection` attack and although this did not return
      anything exciting the search request was accepted and processed with response.

#. In the **Search field** enter :guilabel:`<script>alert("Your system is infected! Call 999-888-7777 for help.")</script>` and press **Enter**

   .. image:: ./images/searchscript.png
     :height: 150px

   .. image:: ./images/searchscriptresult.png
     :height: 150px

   .. NOTE::

      This is a common :guilabel:`Cross-site scripting (XSS)` attack and although this did not return
      anything exciting the search request was accepted and processed with response.

      Also some modern versions of browsers will block this request from displaying a response, but the request was actually sent to the application.  If Chrome blocks it you can try on another browser.

