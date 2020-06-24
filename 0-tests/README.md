# Test Data

## About the directory

This directory contains a script (meta-writer.py) to generate corrupted 360 photo and video files for testing.

[It is inspired by the test scripts in Mapillary tools](https://github.com/mapillary/mapillary_tools/tree/master/mapillary_tools/test).

The `meta-writer.py` outputs are based on valid metadata from photo, timelapse (directory of photos), or mp4 video files (must have telemetry track for GPS modifications).

Here are some examples you can use with the script (taken using a GoPro Fusion camera):

* [photo](/gopro/files/MULTISHOT_0611_000000.jpg)
* [photo directory (timelapse)](/0-tests/files/timelapse/)
* [video](/gopro/files/VIDEO_7152.txt)

## OS Requirements

Works on Windows, Linux and MacOS.

## Installation

* Python version 3.6+
* [exiftool](https://exiftool.org/)
* [ffmpeg](https://www.ffmpeg.org/)

## How it works

You specify if you want to generate an image, directory of images (timelapse) or video files and how it should be corrupted for testing.

The script will use the inputtted hoto, timelapse (directory of photos), or mp4 video file as a template, and corrupt as specified.

* strip all metadata (`-1`)
	- description: creates file(s) (from template) with all metadata removed
	- output: video, photo
* strip telemetry track (`-2`)
	- description: creates file (from template) with all gps metadata from the video telemetry track (gmpf) removed
	- output: video
* corrupt (add invalid co-ordinates) all GPS lat / lon (`-3`)
	- description: creates file(s) (from template) with co-ordinates but all coordinates are invalid (not resolvable). `GPSDateTime` and `GPSaltitude` remains unchanged.
	- output: photo
* randomise (add any valid co-ordinates) all GPS lat / lon (`-4`)
	- description: creates file(s) (from template) with any valid co-ordinates (resolvable). `GPSDateTime` and `GPSaltitude` remains unchanged.
	- output: photo
* Remove xmp equirectangular tag (`-5`)
	- description: creates file(s) (from template) with this tag value removed from metadata
	- output: video, photo
* image larger than 100 megapixels (`-6`)
	- description: create file(s) (from template) with width = 12,000 and height = 9,000 (and reported in metadata)
	- output: photo
* image smaller than 8.5 megapixed (4k) (`-7`)
	- description: create file(s) (from template) with width = 2,560 and height = 1,440 (and reported in metadata)
	- output: photo
* image larger than 100MB (`-8`)
	- description: create .jpg file(s) (from template) with data size of 101mb.
	- output: photo
* make images black (`-9`)
	- description: create file(s) (from template) which replaces images (or 20% of video) with black screen with original image dimensions
	- output: video, photo
* change capture times  (`-10`)
	- description: changes all `*createdates` for video and `originaldatetime` for photos to any valid time in past. If timelapse output, photos are spaced at random offset time intervals (between 1 seconds and 30 seconds apart from t=0)
	- output: video, photo
* change gps times  (`-111`)
	- description: changes all `GPSDateTime` to any valid time in past. If timelapse output, photos are spaced at random offset time intervals (between 1 seconds and 30 seconds apart from t=0). If video, all `GPSDateTime` values are offset by same amount from t=0.
	- output: video, photo

## Examples

**Format**

```
python meta-writer.py INPUT_DIRECTORY -CORRUPTION_METHOD OUTPUT_DIRECTORY
```

**Strip all metadata (`-1`) from file MULTISHOT_0611_000000.jpg and output in corrupted directory**

```
python meta-writer.py /gopro/files/MULTISHOT_0611_000000.jpg -1 /gopro/files/corrupted
```

**Make 20% of video frames black (`-9`) in file VIDEO_7152.mp4 and output in corrupted directory**

```
python meta-writer.py /gopro/files/gopro/files/VIDEO_7152.mp4 -9 /gopro/files/corrupted
```

**Rewrite all co-ordinates as new valid co-ordinates (`-4`) for files in directory /0-tests/files/timelapse/ and output in corrupted directory**

```
python meta-writer.py /0-tests/files/timelapse/ -4 /gopro/files/corrupted
```