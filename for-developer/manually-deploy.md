# Manually Deploy

OK, let's access to **Quick Deploy** folder, you will see the following files and subfolders,  don't be dazzled.

![](../.gitbook/assets/image%20%2824%29.png)

Access to build/config/ folder, open config.js file with any text editor, the only thing you need to change is replace the website URL to your WordPress site link.  There's another configuration file is called manifest.json, you can refer to this [section](https://mostore.mofect.io/configure-app/manifest-configuration) to know what manifest.json is.

You can also replace the favicon.png to yours, it will show up on the address bar of the browser.

![](../.gitbook/assets/image%20%2830%29.png)

Then, please upload the whole '**Quick Deploy**' folder to your server, and rename the folder. The details of steps as below:

#### Deploy in subfolder:

If you want to deploy the mobile App under the subfolder and access it via https://domain.com/mobile. Just rename the folder to "mobile", then upload it to your WordPress installation root folder.

#### Deploy as subdomain:

You can also deploy the App as a separate sub-site and access it via https://m.domain.com.  Upload the 'build' folder to anywhere on your server, let's suppose to upload it to /home/domain/mobile folder.

Then, use this path as the root directory to create a new sub-site with your hosting panel or SSH \(if you use unmanaged VPS\). 

