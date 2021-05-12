## Installation
{: id="20210104091404-emngxx4" updated="20210302223517"}

1. {: id="20210104091404-9xegv8y"}Get the icon and unzip
   {: id="20210302223515-79ps3is"}
2. {: id="20210104091404-8gdxzud"}<kbd>Settings</kbd> - <kbd>Appearance</kbd> - <kbd>Icon</kbd> - <kbd>Open Icon Folder</kbd>
   {: id="20210302223515-wu4teq3"}
3. {: id="20210104091404-90wpjja"}Copy the icon to this directory
   {: id="20210302223515-kkr2m9t"}
4. {: id="20210104091404-gcbhyp5"}Restart, select the installed icon in <kbd>Settings</kbd> - <kbd>Appearance</kbd> - <kbd>Icon</kbd>
   {: id="20210302223515-lg2ramr"}
{: id="20210104091404-5mpe4db"}

## Development
{: id="20210104091404-c14ff87"}

### Step
{: id="20210104091404-5ele7ot"}

1. {: id="20210104091404-qgd4dqd"}Give your icon a nice name, such as `alice`
   {: id="20210104091404-gb7rp9u"}
2. {: id="20210104091404-d8cdoqz"}<kbd>Settings</kbd> - <kbd>Appearance</kbd> - <kbd>Icon</kbd> - <kbd>Open Icon Folder</kbd>
   {: id="20210104091404-coh56bo"}
3. {: id="20210104091404-wdwknqi"}Create a new folder `alice` in the opened folder, and create new `icon.js` and `icon.json` files in `alice` The `icon.json` file is as follows:
   {: id="20210104091404-0errb7b"}

   ```json
   {
     "author": "Vanessa",
     "url": "https://github.com/Vanessa219",
     "version": "1.0.0"
   }
   ```
   {: id="20210104091404-olba0a3"}
4. {: id="20210104091404-swh87z4"}Open the `icon.js` file and paste the completed icon
   {: id="20210104091404-affafn6"}
5. {: id="20210104091404-ivd5l04"}Restart, select the installed icon in <kbd>Settings</kbd> - <kbd>Appearance</kbd> - <kbd>Icon</kbd>
   {: id="20210104091404-9c6o5ow"}
{: id="20210104091404-07yula4"}

### Icon production
{: id="20210104091404-4c1epvw"}

* {: id="20210104091404-ioq4e81"}Use a browser to open the `index.html` file in the icon folder
  {: id="20210104091404-tt2x38y"}
* {: id="20210104091404-k2l5fm9"}Make similar icons based on the icon name and shape
  {: id="20210104091404-yyxvz0t"}

  * {: id="20210104091404-2i6izha"}Go to [Iconfont](https://www.iconfont.cn) to search for your favorite icon and download the SVG format
    {: id="20210302223515-tyeicmf"}
  * {: id="20210104091404-ohj824d"}Use vector graphics tools to make your own icons in SVG format
    {: id="20210302223515-ejgdtps"}
  * {: id="20210104091404-4tobq3m"}Go to [pngtosvg](https://www.pngtosvg.com/) to convert the picture to SVG format
    {: id="20210302223515-l0fwwjj"}
  {: id="20210104091404-tv40w1x"}
* {: id="20210104091404-dkmivym"}Go to [IcoMoon App](https://icomoon.io/app/#/select) to make `icon.js`
  {: id="20210104091404-foonnfg"}

  * {: id="20210104091404-08zo0iy"}Click on `Import Icons` in the upper right corner to import the pictures made in the previous step
    {: id="20210302223515-3y0helv"}
  * {: id="20210104091404-qvg4wjs"}Select the icon and generate SVG
    ![image.png](assets/image.png)
    {: id="20210302223515-mcj3t59"}
  * {: id="20210104091404-eds5a8k"}Modify the size and download
    ![image.png](assets/image-krr52x1.png)
    {: id="20210302223515-gaemr53"}
  * {: id="20210104091404-emihiqw"}Modify the `id` in `<symbol id="icon-markdown" viewBox="0 0 32 32">` to the icon name corresponding to `index.html`
    {: id="20210302223515-o22v67z"}
  * {: id="20210104091404-m0zpn8g"}Replace the content in `<defs>...</defs>` to the corresponding position in `icon.js`
    {: id="20210302223515-sf1sm6z"}
  {: id="20210104091404-rfqjpsy"}
* {: id="20210104091404-s8l7xu3"}Test
  {: id="20210104091404-bhbfkps"}

  * {: id="20210104091404-0cijd7s"}Replace `material` in `index.html` with `alice`
    {: id="20210104091404-azquhxu"}

    ```html
    <script src="material/icon.js"></script>
    ```
    {: id="20210104091404-ysvipkm"}
  * {: id="20210104091404-jx50ge9"}Refresh `index.html` to see the final result
    {: id="20210104091404-shk25pp"}
  * {: id="20210104091404-hgd591a"}Open SiYuan and select the developed icon in <kbd>Settings</kbd> - <kbd>Appearance</kbd> - <kbd>Icon</kbd> to view
    {: id="20210104091404-8v71h8q"}
  {: id="20210104091404-pvo2ori"}
* {: id="20210104091404-9ju8k2d"}Released on the shelf (contact QQ: 84588990)
  {: id="20210104091404-x35pum5"}
{: id="20210104091404-ewdyw7f"}


{: id="20200924100110-vcg96wy" type="doc"}
