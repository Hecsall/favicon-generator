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
