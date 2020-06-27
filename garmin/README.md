# Garmin Metadata

## Garmin Cameras

1. [Garmin VIRB 360](https://buy.garmin.com/en-GB/GB/p/562010)

### Metadata DB

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

#### ga01

* Make/model: Garmin VIRB 360
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: False
* Reports pitch / heading EXIF: False
* Is geotagged by cam: TRUE
* filename: V5660909.JPG
* Date updated: 2020-06-21


[V5660909.JPG](/garmin/files/V5660909.JPG)

```
exiftool -G -s -b -j -a -T V5660909.JPG > garmin_virb_360_V5660909_timelapse_metadata.json
```

[garmin_virb_360_V5660909_timelapse_metadata.json](/garmin/files/garmin_virb_360_V5660909_timelapse_metadata.json)

#### ga02

* Make/model: Garmin VIRB 360
* Type: Video
	- mp4
* Telemetry track: FALSE (use .fit file)
* Is geotagged by cam: TRUE (creates seperate .fit file)
* filename: V0380038.MP4
* Date updated: 2020-06-21

_Note on .fit file_

Garmin VIRB 360 does not write GPS / telemetry track into the mp4 video file.

The VIRB writes a seperate `.fit` file with GPS telemetry. The attached fit files for the video below are found in 2018-01-11-17-33-54.fit

**Video level data**

[V0380038.MP4](/garmin/files/V0380038.txt)

```
exiftool -ee -G -s -b -j -a -T V0380038.MP4 > garmin_virb_360_V0380038_metadata_overview.json
```

[garmin_virb_360_V0380038_metadata_overview.json](/garmin/files/garmin_virb_360_V0380038_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[V0380038.MP4](/garmin/files/V0380038.txt)

```
exiftool -ee -G3 -s -b -j -a -T V0380038.MP4 > garmin_virb_360_V0380038_metadata_track.json
```

[garmin_virb_360_V0380038_metadata_track.json](/garmin/files/garmin_virb_360_V0380038_metadata_track.json)