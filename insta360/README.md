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

**Video level data**

```
exiftool -ee -G -s -b -j -a -T insta-pro-002.mp4 > insta360_pro_insta-pro-002_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T insta-pro-002.mp4 > insta360_pro_insta-pro-002_metadata_track.json
```
