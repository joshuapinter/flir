# FLIR

## Manipulate FLIR IR images.

Completely based on tomas123's flir.php file. Instead of being locked away in inaccessible forums, it's here for improvement and reporting.

## Usage

```bash
$ php flir.php         # or
$ php flir.php -h      # or
$ php flir.php --help

usage: $argv[0] [options] -i ir_file.jpg -o outputimage

Settings:
-i ir_file.jpg      flir radiometric image
-o output.jpg       save  8 Bit image jpg
-o output.png       save 16 Bit image png

Options Summary:
--resize val        scale sensor size with "convert -resize val" (val i.e. 600x or 100%, default is 200%)
--tref temp         overwrite embedded Reflected Apparent Temperature (degree Celsius) 
--emis val          overwrite embedded Emissivity (val i.e. 0.95)
--rmin raw_min      set min RAW value instead embedded value (set scale min temp)
--rmax raw_ma       set max RAW value instead embedded value (set scale max temp)
--pal iron.png      use own palette (instead of embedded palette.png)
--clut              disable "Color LookUp Table" and color scale (save a grayscale image)
--scale             disable color scale on the right edge
--pip[=AxB]         input image is a flir PiP radiometric image
                    overlay embedded "real image" with "ir image"
                    [optional] crop ir image to size AxB (i.e. --pip=90x90 )
--help              print this help
```  

## Reference 

###[tomas123's original PHP script](http://u88.n24.queensu.ca/exiftool/forum/index.php/topic,4898.0.html)

This was the original (lengthy) thread where user tomas123 originally posted the flir.php script. In this entire thread you can see 
that tomas123 really knows his way around images, thermal imaging, ImageMagick and coding. Very impressive. This Github repository is solely 
a means to allow more people to see his work and hopefully to improve and expand upon it. Hopefully, tomas123 will even come on here and 
contribute (or take ownership).

###[BFIC Image Editor by Daves](http://pc.daves.cz/BFIC_-_thermal_images)

"Daves" used tomas123's original flir.php script and created a very impressive Windows GUI around it, allowing you to do realtime edits of thermal 
images and generate basic reports. In particularly, it allows you to easily:

* change the shown temperature range, 
* change the colour palette,
* add spots and their tempreature, 
* add areas and their temperature ranges,
* export to a CSV file,
* and adjust nearly every single setting.


