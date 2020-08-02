# Insta360 Metadata

## Insta360 360 Cameras

1. [ONE](https://www.insta360.com/product/insta360-one/)
2. [ONE X](https://www.insta360.com/product/insta360-onex/)
3. [ONE R](https://www.insta360.com/product/insta360-oner_1inch-edition)
4. [Pro](https://www.insta360.com/product/insta360-pro/)
5. [Pro2](https://www.insta360.com/product/insta360-pro2/)
6. [Titan](https://www.insta360.com/product/insta360-titan/)

### Metadata DB

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

#### is01

* Make/model: Insta360 Pro
* Type: Video
	- mp4
* Telemetry track: camm
	- camm2, camm3, camm6
* Is geotagged by cam: TRUE
* filename: insta-pro-002.mp4
* Date updated: 2020-06-21
* Is 360: True

**Video level data**

[insta-pro-002.mp4](/insta360/files/insta-pro-002.txt)

```
exiftool -ee -G -s -b -j -a -T insta-pro-002.mp4 > insta360_pro_insta-pro-002_metadata_overview.json
```

[insta360_pro_insta-pro-002_metadata_overview.json](/insta360/files/insta360_pro_insta-pro-002_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[insta-pro-002.mp4](/insta360/files/insta-pro-002.txt)

```
exiftool -ee -G3 -s -b -j -a -T insta-pro-002.mp4 > insta360_pro_insta-pro-002_metadata_track.json
```

[insta360_pro_insta-pro-002_metadata_track.json](/insta360/files/insta360_pro_insta-pro-002_metadata_track.json)

#### is02

* Make/model: Insta360 Pro
* Type: Photo


#### is03

* Make/model: Insta360 Titan
* Type: Video
	- mp4
* Telemetry track: camm
	- camm1, camm2, camm3, camm6
* Is geotagged by cam: TRUE
* filename: VID_20200620_Faster_75.mp4
* Date updated: 2020-06-23
* Is 360: True

**Video level data**

[VID_20200620_Faster_75.mp4](/insta360/files/VID_20200620_Faster_75.txt)

```
exiftool -ee -G -s -b -j -a -T VID_20200620_Faster_75.mp4 > insta360_titan_VID_20200620_Faster_75_metadata_overview.json
```

[insta360_titan_VID_20200620_Faster_75_metadata_overview.json](/insta360/files/insta360_titan_VID_20200620_Faster_75_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[VID_20200620_Faster_75.mp4](/insta360/files/VID_20200620_Faster_75.txt)

```
exiftool -ee -G3 -s -b -j -a -T VID_20200620_Faster_75.mp4 > insta360_titan_VID_20200620_Faster_75_metadata_track.json
```

[insta360_titan_VID_20200620_Faster_75_metadata_track.json](/insta360/files/insta360_titan_VID_20200620_Faster_75_metadata_track.json)

#### is04

* Make/model: Insta360 Titan
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: False
* Reports pitch / heading EXIF: False
* Is geotagged by cam: TRUE
* filename: GSAG2002.jpg
* Date updated: 2020-06-21
* Is 360: True

[PIC_20200620_161820_20_06_22_09_38_21_output_009.jpg](/insta360/files/PIC_20200620_161820_20_06_22_09_38_21_output_009.jpg)

```
exiftool -G -s -b -j -a -T PIC_20200620_161820_20_06_22_09_38_21_output_009.jpg > insta360_titan_PIC_20200620_161820_20_06_22_09_38_21_output_009_timelapse_metadata.json
```

[insta360_titan_PIC_20200620_161820_20_06_22_09_38_21_output_009_timelapse_metadata.json](/insta360/files/insta360_titan_PIC_20200620_161820_20_06_22_09_38_21_output_009_timelapse_metadata.json)