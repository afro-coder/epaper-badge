# Pico 2.7 ePaper Code

This is a badge I made using the waveshare 2.7 inch ePaper pico display

The `fbimage.py` is used to convert images from pbm to bytecode in the Framebuffer format. I found it from this [repository](https://github.com/JPFrancoia/esp32_devkit_waveshare_eink_screen).

To display images on the e-paper, we have to first convert the image to Black and White I used Gimp to do that.
- In Gimp open the image => Go to the Image Option
  Click on Mode => Indexed => Select Black and white mode

- Then make sure to scale the image to the size you want it to be.
- Save the image as `bmp` and then go to the command line, you'll need imagick for this.
```
convert image.bmp image.pbm
```

- Once you export the image to bmp, run the python script `python fbimage.py image.pbm`

Then copy the hexdump and add it to your script and you'll be able to display images.
