# Test Data

## About the directory

This directory contains a script (meta-writer.py) to generate corrupted 360 photo and video files for testing.

[It is inspired by the test scripts in Mapillary tools](https://github.com/mapillary/mapillary_tools/tree/master/mapillary_tools/test).

The `meta-writer.py` outputs are based on valid metadata from GoPro Fusion files:

* [image](/gopro/files/MULTISHOT_0611_000000.txt)
* [timelapse](/0-tests/files/timelapse/)
* [video](/gopro/files/VIDEO_7152.txt)

## Installation

* Python version 3.6+
* [exiftool](https://exiftool.org/)
* [ffmpeg](https://www.ffmpeg.org/)

## How it works

You specify if you want to generate an image, directory of images or video files and what metadata should be corrupted for testing.

* strip all metadata
	- video, timelapse photos, single photo
* strip telemetry track
	- video
* corrupt (add invalid co-ordinates) all GPS lat / lon
	- video, single photo
* corrupt (add invalid co-ordinates) random GPS lat / lon
	- video, timelapse photos
* randomise (add any valid co-ordinates) all GPS lat / lon
	- video, single photo
* randomise (add any valid co-ordinates) some GPS lat / lon
	- video, timelapse photos
* Remove xmp equirectangular tag
	- video, timelapse photos, single photo
* image larger than 100 megapixels (images only)
	- single photo
* image smaller than 8.5 megapixed (4k) (images only)
	- single photo
* image larger than 100MB (images only)
	- single photo
* make all image black
	- video, single photo
* make random images black
	- timelapse