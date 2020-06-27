# Labpano Pilot Metadata

## Labpano Pilot 360 Cameras

1. [Labpano Pilot One](https://www.labpano.com/one)
2. [Labpano Pilot Era](https://pilot.labpano.com/)
3. [Labpano Pilot Lock](https://www.labpano.com/lock)

### Metadata DB

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

#### lp01

* Make/model: LabPano Pilot Era
* Type: Video
	- mp4
* Telemetry track: camm
	- camm2, camm3, camm6
* Is geotagged by cam: FALSE (requires external module/app)
* filename: 200207_085206318.mp4
* Date updated: 2020-06-21

**Video level data**

[200207_085206318.mp4](/labpano/files/200207_085206318.txt)

```
exiftool -ee -G -s -b -j -a -T 200207_085206318.mp4 > labpano_pilot_era_200207_085206318_metadata_overview.json
```

[labpano_pilot_era_200207_085206318_metadata_overview.json](/labpano/files/labpano_pilot_era_200207_085206318_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[200207_085206318.mp4](/labpano/files/200207_085206318.txt)

```
exiftool -ee -G3 -s -b -j -a -T 200207_085206318.mp4 > labpano_pilot_era_200207_085206318_metadata_track.json
```

[labpano_pilot_era_200207_085206318_metadata_track.json](/labpano/files/labpano_pilot_era_200207_085206318_metadata_track.json)

#### lp02

* Make/model: LabPano Pilot Era
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: Heading
* Reports pitch / heading EXIF: Heading
* Is geotagged by cam: FALSE (requires external module/app)
* filename: 200207_094350655.jpg
* Date updated: 2020-06-21

[200207_094350655.jpg](/labpano/files/200207_094350655.jpg)

```
exiftool -G -s -b -j -a -T 200207_094350655.jpg > labpano_pilot_era_200207_094350655_timelapse_metadata.json
```

[labpano_pilot_era_200207_094350655_timelapse_metadata.json](/labpano/files/labpano_pilot_era_200207_094350655_timelapse_metadata.json)

#### lp03

* Make/model: LabPano Pilot One
* Type: Video
	- mp4
* Telemetry track: camm
	- camm2, camm3, camm6
* Is geotagged by cam: FALSE (requires external module/app)
* filename: 200619_161801314.mp4
* Date updated: 2020-06-21

**Video level data**

[200619_161801314.mp4](/labpano/files/200619_161801314.txt)

```
exiftool -ee -G -s -b -j -a -T 200619_161801314.mp4 > labpano_pilot_one_200619_161801314_metadata_overview.json
```

[labpano_pilot_one_200619_161801314_metadata_overview.json](/labpano/files/labpano_pilot_one_200619_161801314_metadata_overview.json)

**Track level data (more verbose -- includes telemetry)**

[200619_161801314.mp4](/labpano/files/200619_161801314.txt)

```
exiftool -ee -G3 -s -b -j -a -T 200619_161801314.mp4 > labpano_pilot_one_200619_161801314_metadata_track.json
```

[labpano_pilot_one_200619_161801314_metadata_track.json](/labpano/files/labpano_pilot_one_200619_161801314_metadata_track.json)

#### lp04

* Make/model: LabPano Pilot One
* Type: Photo
	- jpg
* Reports pitch / heading / roll XMP: Heading
* Reports pitch / heading EXIF: Heading
* Is geotagged by cam: FALSE (requires external module/app)
* filename: 200619_161719613.jpg
* Date updated: 2020-06-21

[200619_161719613.jpg](/labpano/files/200619_161719613.jpg)

```
exiftool -G -s -b -j -a -T 200619_161719613.jpg > labpano_pilot_one_200619_161719613_timelapse_metadata.json
```

[labpano_pilot_one_200619_161719613_timelapse_metadata.json](/labpano/files/labpano_pilot_one_200619_161719613_timelapse_metadata.json)