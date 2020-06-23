# Test Data

## About the directory

This directory contains a script (meta-writer.py) to generate corrupted 360 photo and video files for testing.

[It is inspired by the test scripts in Mapillary tools](https://github.com/mapillary/mapillary_tools/tree/master/mapillary_tools/test).

The `meta-writer.py` outputs are based on valid metadata from GoPro Fusion files:

* [photo](/gopro/files/MULTISHOT_0611_000000.jpg)
* [photo directory (timelapse)](/0-tests/files/timelapse/)
* [video](/gopro/files/VIDEO_7152.txt)

## Installation

* Python version 3.6+
* [exiftool](https://exiftool.org/)
* [ffmpeg](https://www.ffmpeg.org/)

## How it works

You specify if you want to generate an image, directory of images or video files and what metadata should be corrupted for testing.

* strip all metadata
	- description: creates file(s) (from template) with all metadata removed
	- output: video, photo
* strip telemetry track
	- description: creates file (from template) with all gps metadata from the video telemetry track (gmpf) removed
	- output: video
* corrupt (add invalid co-ordinates) all GPS lat / lon
	- description: creates file(s) (from template) with co-ordinates but all coordinates are invalid (not resolvable)
	- output: photo
* randomise (add any valid co-ordinates) all GPS lat / lon
	- description: creates file(s) (from template) with any valid co-ordinates (resolvable)
	- output: photo
* Remove xmp equirectangular tag
	- description: creates file(s) (from template) with this tag value removed from metadata
	- output: video, photo
* image larger than 100 megapixels (images only)
	- description: create file(s) (from template) with width = 12,000 and height = 9,000 (and reported in metadata)
	- output: photo
* image smaller than 8.5 megapixed (4k) (images only)
	- description: create file(s) (from template) with width = 2,560 and height = 1,440 (and reported in metadata)
	- output: photo
* image larger than 100MB (images only)
	- description: create .jpg file(s) (from template) with data size of 101mb.
	- output: photo
* make all images black
	- description: create file(s) (from template) which replaces image with black screen with original image dimensions
	- output: video, photo