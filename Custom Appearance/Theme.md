## Installation
{: id="20201225174048-t626xpi"}

1. {: id="20201225174048-ojae0rn"}Get the theme and unzip
2. {: id="20201225174048-pw7h495"}In SiYuan, click Settings - Appearance - Theme - Open theme folder
3. {: id="20201225174048-b505cz4"}Copy the theme to this directory
4. {: id="20201225174048-wcls1ma"}After restarting SiYuan, select the installed theme in Settings - Appearance - Theme
{: id="20201225174048-ur54two"}

## Development
{: id="20201225174048-i781zxp"}

### Step
{: id="20201225174048-3qumvw6"}

1. {: id="20201225174048-axf0aph"}Give your subject a nice name, such as `alice`
   {: id="20201225174048-dw4dke4"}
2. {: id="20201225174048-zfkshfl"}In SiYuan, click Settings - Appearance - Theme - Open theme folder
   {: id="20201225174048-1dt9umq"}
3. {: id="20201225174048-92haint"}Create a new folder `alice` in the opened folder, and create new `theme.css` and `theme.json` files in `alice`
   The `theme.json` file is as follows:
   {: id="20201225174048-fh16r64"}

   ```json
   {
     "name": "Midnight",
     "author": "Vanessa",
     "version": "1.0.0",
     "modes": ["dark"]
   }
   ```
   {: id="20201225174048-d4ms7ra"}

   `modes` is the appearance mode, divided into `dark` and `light`
   {: id="20201225174048-crkpdob"}
4. {: id="20201225174048-e4e9234"}Open the `theme.css` file to start your coding journey
   {: id="20201225174048-2937fh2"}
5. {: id="20201225174048-sw6gvxg"}After restarting SiYuan, select the installed theme in Settings - Appearance - Theme
   {: id="20201225174048-xii3128"}
{: id="20201225174048-zqtzaox"}

### Encoding
{: id="20201225174048-5e5cg0p"}

* {: id="20201225174048-tt2mbf7"}Familiar with [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS) basic knowledge
* {: id="20201225174048-1ocyqbk"}Modify the color scheme in `:root{...}`
* {: id="20201225174048-c3hch71"}Continue to modify according to steps 1-4 in the figure
  ![image.png](assets/image-bozvb00.png)
* {: id="20201225174048-9mhz3ye"}Copy and paste the modified content into `theme.css` and save
* {: id="20201225174048-k5l65hd"}Check the `Disable cache` in `Network` and run `window.location.reload()` to see the final result
  ![image.png](assets/image-9b9y2ky.png)
* {: id="20201225174048-wxq2ri1"}Released on the shelf (contact QQ: 84588990)
{: id="20201225174048-g8oxi84"}


{: id="20200924095938-a9p5450" type="doc"}
