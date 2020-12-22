## Installation

1. Get the icon and unzip
2. Click Settings - Appearance - Icon - Open Icon Folder in SiYuan
3. Copy the icon to this directory
4. After restarting SiYuan, select the installed icon in Settings - Appearance - Icon

## Development

### Step

1. Give your icon a nice name, such as `alice`
2. Click Settings - Appearance - Icon - Open Icon Folder in SiYuan
3. Create a new folder `alice` in the opened folder, and create new `icon.js` and `icon.json` files in `alice` The `icon.json` file is as follows:

   ```json
   {
     "author": "Vanessa",
     "url": "https://github.com/Vanessa219"
     "version": "1.0.0"
   }
   ```
4. Open the `icon.js` file and paste the completed icon
5. After restarting SiYuan, select the installed icon in Settings - Appearance - Icon

### Icon production

* Use a browser to open the `index.html` file in the icon folder
* Make similar icons based on the icon name and shape

  * Go to [Iconfont](https://www.iconfont.cn) to search for your favorite icon and download the SVG format
  * Use vector graphics tools to make your own icons in SVG format
  * Go to [pngtosvg](https://www.pngtosvg.com/) to convert the picture to SVG format
* Go to [IcoMoon App](https://icomoon.io/app/#/select) to make `icon.js`

  * Click on `Import Icons` in the upper right corner to import the pictures made in the previous step
  * Select the icon and generate SVG
    ![image.png](assets/image.png)
  * Modify the size and download
    ![image.png](assets/image-krr52x1.png)
  * Modify the `id` in `<symbol id="icon-markdown" viewBox="0 0 32 32">` to the icon name corresponding to `index.html`
  * Replace the content in `<defs>...</defs>` to the corresponding position in `icon.js`
* Test

  * Replace `material` in `index.html` with `alice`

    ```html
    <script src="material/icon.js"></script>
    ```
  * Refresh `index.html` to see the final result
  * Open SiYuan and select the developed icon in Settings - Appearance - Icon to view
* Released on the shelf (contact QQ: 84588990)


{: id="20200924100110-vcg96wy" type="doc"}