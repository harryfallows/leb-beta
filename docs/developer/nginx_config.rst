NGINX Configuration Page
-------------------------

The NGINX configuration page, available at the "local_enterobase/nginx_config" endpoint, is designed to enable the installer to obtain an "nginx.conf" file without having to write one from scratch. The user must simply input some basic details and the web-page returns the "nginx.conf" file. To read more about how the page looks from the point of view of the user, please take a look at the following page in the installation documentation: :ref:`nginx-prerequisites-label>`. All code relating to this page is available in the "entero/local_enterobase" directory of the Central EnteroBase repository.

There is more information regarding the contents of the "nginx.conf" file available at: http://nginx.org/en/docs/http/ngx_http_core_module.html.

.. figure:: ../images/nginx_config_page.png
   :width: 600
   :align: center
   :alt: Local EnteroBase Registration Form

   **Fig. 1 - NGINX Configuration Form**

The above figure shows a screenshot of what the user sees when they go to the page. Below is a list of the validations enforced by the FlaskForm used to handle the input:

1. Local EnteroBase Name: check if unique (no other instance with the same name) and between 1 and 64 characters.
2. External URL: check if unique (no other instance with the same URL) and valid URL or IP with "https".
3. Description & Justification: check if between 0 and 400 characters.
4. Central EnteroBase Username of Local EnteroBase Admin: check if unique (admin has no other Local EnteroBase instances) and user is logged in as admin.

