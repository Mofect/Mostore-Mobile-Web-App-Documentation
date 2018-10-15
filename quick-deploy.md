---
description: >-
  If you just want to quick deploy the app without customize the app templates,
  please follow this guide. It's super easy.
---

# Quick Deploy

## Unzip The Package File

Unzip the package file which you have downloaded, you will get these two folders:

* App
* WordPress Helper Plugin
* Quick Deploy

Mostore source files are included in the _**App**_ folder, the deploy files are included in the _**Quick Deploy**_ folder and another part is a helper plugin which is called "Mofect Mobile Assistant", it's included in the _**WordPress Helper Plugin**_ folder.

### Upload APP Files To Your Server

OK, let's access to **Quick Deploy** folder, you will see the following files and subfolders,  don't be dazzled.

![](.gitbook/assets/image%20%2821%29.png)

Access to build/config/ folder, open config.js file with any text editor, the only thing you need to change is replace the website URL to your WordPress site link.  There's another configuration file is called manifest.json, you can refer to this [section](https://mostore.mofect.io/configure-app/manifest-configuration) to know what manifest.json is.

You can also replace the favicon.png to yours, it will show up on the address bar of the browser.

![](.gitbook/assets/image%20%2827%29.png)

Then, please upload the whole '**Quick Deploy**' folder to your server, and rename the folder. The details of steps as below:

#### Deploy in subfolder:

If you want to deploy the mobile App under the subfolder and access it via https://domain.com/mobile. Just rename the folder to "mobile", then upload it to your WordPress installation root folder.

#### Deploy as subdomain:

You can also deploy the App as a separate sub-site and access it via https://m.domain.com.  Upload the 'build' folder to anywhere on your server, let's suppose to upload it to /home/domain/mobile folder.

Then, use this path as the root directory to create a new sub-site with your hosting panel or SSH \(if you use unmanaged VPS\). 

### Install Mofect Mobile Assistant Plugin

The next important step is install Mofect Mobile Assistant plugin on your WordPress. This helper plugin offers some import extended REST API endpoints to makes the Mobile App launch as normal.

* Log in your WordPress backend with administrator account. 
* Go to Plugins &gt; Install plugin page, upload mofect-mobile-assistant.zip file and activate the plugin.

Once the plugin is activated, the page will be redirected to the Authentication screen. 

![](.gitbook/assets/auth_wc.png)

Before you click the big button to connect App to your WooCommerce, you should know the following tips:

* 1. For security reason, your website must enable SSL, otherwise, the authentication process will be failed. You can simply use the free SSL certificate from [Let’s Encrypt](https://letsencrypt.org/).
* 2. You must log in the administrator account.
* 3. You can cancel the authentication at any time by clicking the "Disconnect" button. Then, your WooCommerce consumer key and secret will be automatically deleted. Of course, you can still one click to rebuild the new connection.
* 4. Once you deactivate or uninstall Mofect Mobile Assistant plugin, your WooCommmerce consumer key and secret will be automatically deleted, it means you have to reconnect the mobile web app to your WooCommerce store if you reactivate this plugin.
* **4. We strongly suggest you rebuild the connection regularly.**

OK, do it! Click the connect button, and approve the authentication request.

![](.gitbook/assets/auth_wc_approve%20%281%29.png)

That's it! Now, you can access to your mobile APP via the subdomain or subfolder, and all products, posts is synced to the mobile App automatically.

OK, in the next section, we will introduce you how to configure the App with Mofect Mobile Assistant plugin.

