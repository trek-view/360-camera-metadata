# Ricoh Metadata

## Ricoh 360 Cameras

1. [Theta V](https://theta360.com/en/about/theta/v.html)
2. [Theta Z1](https://theta360.com/en/about/theta/z1.html)

### Metadata DB

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

#### th01

* Make/model: Ricoh Theta V
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: Record exists but show 0
* Reports pitch / heading EXIF: FALSE
* Is geotagged by cam: FALSE (requires external module/app)
* filename:  R0014760.jpg
* Date updated: 2020-06-21

[R0014760.JPG](/ricoh/files/R0014760.JPG)

```
exiftool -G -s -b -j -a -T R0014760.jpg > theta_v_R0014760_timelapse_metadata.json
```

[theta_v_R0014760_timelapse_metadata.json](/ricoh/files/theta_v_R0014760_timelapse_metadata.json)

#### th02

* Make/model: Ricoh Theta V
* Type: Video
	- mp4
* Telemetry track: camm
	- camm2, camm3
* Is geotagged by cam: FALSE (requires external module/app)
* filename: 20200511_113008_255.mp4
* Date updated: 2020-06-21

_Seems that the Theta V only includes camm2 and camm3 in the camm track -- no lat / lon GPS telemetry (camm5 / camm6). Not 100% sure what is going on here (can positional data be calculated using camm2+3?)_

**Video level data**

[20200511_113008_255.mp4](/ricoh/files/20200511_113008_255.txt)

```
exiftool -ee -G -s -b -j -a -T 20200511_113008_255.mp4 > theta_v_20200511_113008_255_metadata_overview.json
```

[theta_v_20200511_113008_255_metadata_overview.json](/ricoh/files/theta_v_20200511_113008_255_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[20200511_113008_255.mp4](/ricoh/files/20200511_113008_255.txt)

```
exiftool -ee -G3 -s -b -j -a -T 20200511_113008_255.mp4 > theta_v_20200511_113008_255_metadata_track.json
```

[theta_v_20200511_113008_255_metadata_track.json](/ricoh/files/theta_v_20200511_113008_255_metadata_track.json)

#### th03

* Make/model: Ricoh Theta Z1
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: Record exists but show 0
* Reports pitch / heading EXIF: FALSE
* Is geotagged by cam: FALSE (requires external module/app)
* filename: R0013798.JPG
* Date updated: 2020-06-21

[R0013798.JPG](/ricoh/files/R0013798.JPG)

```
exiftool -G -s -b -j -a -T R0013798.JPG > theta_z1_R0013798_timelapse_metadata.json
```

[theta_z1_R0013798_timelapse_metadata.json](/ricoh/files/theta_z1_R0013798_timelapse_metadata.json)

#### th04

* Make/model: Ricoh Theta Z1
* Type: Video
	- mp4
* Telemetry track: camm
	- camm2, camm6
* Is geotagged by cam: FALSE (requires external module/app)
* filename: R008000.MP4
* Date updated: 2020-06-21

**Video level data**

[R008000.MP4](/ricoh/files/R008000.txt)

```
exiftool -ee -G -s -b -j -a -T R008000.MP4 > theta_z1_R008000_metadata_overview.json
```

[theta_z1_R008000_metadata_overview.json](/ricoh/files/theta_z1_R008000_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[R008000.MP4](/ricoh/files/R008000.txt)

```
exiftool -ee -G3 -s -b -j -a -T R008000.MP4 > theta_z1_R008000_metadata_track.json
```

[theta_z1_R008000_metadata_overview.json](/ricoh/files/theta_z1_R008000_metadata_track.json)