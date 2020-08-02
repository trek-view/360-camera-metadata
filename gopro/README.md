# GoPro Metadata

## GoPro 360 Cameras

1. [GoPro Fusion (discontinued)](https://gopro.com/en/us/fusion)
2. [GoPro MAX](https://gopro.com/en/us/shop/cameras/max/CHDHZ-201-master.html)

### Metadata DB

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

#### gp01

* Make/model: GoPro MAX
* Type: Video
	- mp4
* Telemetry track: GPMF
* Is geotagged by cam: TRUE
* filename: GS012804.mp4
* Date updated: 2020-06-21
* Is 360: True
* Stitched on: GoPro Player (Mac)

**Video level data**

[GS012804.mp4](/gopro/files/GS012804.txt)

```
exiftool -ee -G -s -b -j -a -T GS012804.mp4 > gopro_max_GS012804_metadata_overview.json
```

[gopro_max_GS012804_metadata_overview.json](/gopro/files/gopro_max_GS012804_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[GS012804.mp4](/gopro/files/GS012804.txt)

```
exiftool -ee -G3 -s -b -j -a -T GS012804.mp4 > gopro_max_GS012804_metadata_track.json
```

[gopro_max_GS012804_metadata_track.json](/gopro/files/gopro_max_GS012804_metadata_track.json)

#### gp02

* Make/model: GoPro MAX
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: False
* Reports pitch / heading EXIF: False
* Is geotagged by cam: TRUE
* filename: GSAG2002.jpg
* Date updated: 2020-06-21
* Is 360: True
* Stitched on: Camera

[GSAG2002.jpg](/gopro/files/GSAG2002.jpg)

```
exiftool -G -s -b -j -a -T GSAG2002.jpg > gopro_max_GSAG2002_timelapse_metadata.json
```

[gopro_max_GSAG2002_timelapse_metadata.json](/gopro/files/gopro_max_GSAG2002_timelapse_metadata.json)

#### gp03

* Make/model: GoPro Fusion
* Type: Video
	- mp4
* Telemetry track: GPMF
* Is geotagged by cam: TRUE
* filename: VIDEO_7152.mp4
* Date updated: 2020-06-21
* Is 360: True
* Stitched on: GoPro Fusion Studio

**Video level data**

[VIDEO_7152.mp4](/gopro/files/VIDEO_7152.txt)

```
exiftool -ee -G -s -b -j -a -T VIDEO_7152.mp4 > gopro_fusion_VIDEO_7152_metadata_overview.json
```

[gopro_fusion_VIDEO_7152_metadata_overview.json](/gopro/files/gopro_fusion_VIDEO_7152_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[VIDEO_7152.mp4](/gopro/files/VIDEO_7152.txt)

```
exiftool -ee -G3 -s -b -j -a -T VIDEO_7152.mp4 > gopro_fusion_VIDEO_7152_metadata_track.json
```

[gopro_fusion_VIDEO_7152_metadata_track.json](/gopro/files/gopro_fusion_VIDEO_7152_metadata_track.json)

#### gp04

* Make/model: GoPro Fusion
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: False
* Reports pitch / heading EXIF: False
* Is geotagged by cam: TRUE
* filename: MULTISHOT_0611_000000.jpg
* Date updated: 2020-06-21
* Is 360: True
* Stitched on: GoPro Fusion Studio

[GSAG2002.jpg](/gopro/files/MULTISHOT_0611_000000.jpg)

```
exiftool -G -s -b -j -a -T MULTISHOT_0611_000000.jpg > gopro_fusion_MULTISHOT_0611_000000_timelapse_metadata.json
```

[gopro_fusion_MULTISHOT_0611_000000_timelapse_metadata.json](/gopro/files/gopro_fusion_MULTISHOT_0611_000000_timelapse_metadata.json)

#### gp05

* Make/model: GoPro MAX
* Type: Video
	- mp4
* Telemetry track: GPMF
* Is geotagged by cam: TRUE
* filename: GH010120.MP4
* Date updated: 2020-08-02
* Is 360: FALSE
* Stitched on: Camera

**Video level data**

[GH010120.MP4](/gopro/files/GH010120.txt)

```
exiftool -ee -G -s -b -j -a -T GH010120.mp4 > gopro_max_hero_GH010120_metadata_overview.json
```

[gopro_max_hero_GH010120_metadata_overview.json](/gopro/files/gopro_max_hero_GH010120_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[VIDEO_7152.mp4](/gopro/files/VIDEO_7152.txt)

```
exiftool -ee -G3 -s -b -j -a -T GH010120.mp4 > gopro_max_hero_GH010120_metadata_track.json
```

[gopro_max_hero_GH010120_metadata_track.json](/gopro/files/gopro_max_hero_GH010120_metadata_track.json)
