Giffer
======

A Bash script to convert a video file to an animated GIF.

Puts an emphasis on simplicity of use and quality of the GIF. I wrote it because I was stuggling to find an alternative method that provided these benefits. I tried using `ffmpeg` on its own for example, but I could never get the quality of the GIF quite right. The recommendation seemed to be to export to still frames first, then use ImageMagick to convert the frames to a GIF – which is exactly what this script does.


Installation
------------

You'll need to have ffmpeg and ImageMagick installed. You can do that on a Mac by installing [Homebrew](http://brew.sh/) and then doing:

	brew install imagemagick ffmpeg

Then to get the script itself you can do:

	git clone git@github.com:paulherron/giffer.git

You can copy the script to your preferred location, or symlink it into place.


Usage
-----

The simplest way to use it is like:

	giffer -i my_video.mp4

There are other options too, which you can see by doing:

	giffer -h

To give an idea of the options available, here's an example command that sets custom input and output names, conversion method and frame rate, and prompts you before generating the file:

	giffer -i custom_file.mp4 -o final.gif -r 10 -m optimize -c
