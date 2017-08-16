# Favicon Generator
This python script generates different sizes favicons from one image.
For good results, the original image should be a perfect square, 600x600 px and NOT smaller.

**NOTICE: only tested with Python 3**


## Dependency
This script requires Pillow and PILkit to manage the images.
* pip install Pillow
* pip install pilkit


## Usage
python3 faviconGenerator.py [-h] [-o OUTPUT] originalimage [originalimage ...]

Examples:
* python3 faviconGenerator.py -o someFolder yourFavicon.png
* python3 faviconGenerator.py yourFavicon.png (will write to "faviconGenerator" folder)
* python3 faviconGenerator.py -o . yourFavicon.png (will write to the same folder of the script)

#### Positional arguments:

* **originalimage**  Starting base image, needs to be a perfect square, at least 600x600 px


#### Optional arguments:

* **-h, --help**  show this help message and exit
* **-o OUTPUT, --output OUTPUT**  Directory name where the script saves the images. Default directory name will be "faviconGenerator"


## Nice to know
Using the **-o** argument, will eventually remove leading "**/**" to prevent the script to write in your root directory for security purposes.
You will still be able to write paths like "**-o ../someFolder**".



#### HTML Code
This will be the HTML you will put inside your <head> tag

```HTML
<!-- generics -->
<link rel="icon" href="/path/to/favicon-32.png" sizes="32x32">
<link rel="icon" href="/path/to/favicon-57.png" sizes="57x57">
<link rel="icon" href="/path/to/favicon-76.png" sizes="76x76">
<link rel="icon" href="/path/to/favicon-96.png" sizes="96x96">
<link rel="icon" href="/path/to/favicon-128.png" sizes="128x128">
<link rel="icon" href="/path/to/favicon-228.png" sizes="228x228">

<!-- Android -->
<link rel="shortcut icon" sizes="196x196" href="/path/to/favicon-196.png">

<!-- iOS -->
<link rel="apple-touch-icon" href="/path/to/favicon-120.png" sizes="120x120">
<link rel="apple-touch-icon" href="/path/to/favicon-152.png" sizes="152x152">
<link rel="apple-touch-icon" href="/path/to/favicon-180.png" sizes="180x180">

<!-- Windows 8 IE 10 -->
<meta name="msapplication-TileColor" content="#FFFFFF">
<meta name="msapplication-TileImage" content="/path/to/favicon-144.png">

<!-- Windows 8.1 + IE11 and above -->
<meta name="msapplication-config" content="/path/to/ieconfig.xml" />
```

And this will be your **ieconfig.xml** for Windows 10 Start Menu Tiles (change image paths)
```XML
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
  <msapplication>
    <tile>
      <square70x70logo src="/path/to/smalltile.png"/>
      <square150x150logo src="/path/to/mediumtile.png"/>
      <wide310x150logo src="/path/to/widetile.png"/>
      <square310x310logo src="/path/to/largetile.png"/>
      <TileColor>#009900</TileColor>
    </tile>
  </msapplication>
</browserconfig>
```

#### Some credits
Favicons sizes took from the [favicon-cheat-sheet](https://github.com/audreyr/favicon-cheat-sheet)
