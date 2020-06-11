# Garmin Metadata

## Garmin Cameras

1. [Garmin VIRB 360](https://buy.garmin.com/en-GB/GB/p/562010)

### Metadata DB

| id   | data_added | manufacturer | model  | type      | is_geotagged_by_cam | sample_file |
|------|------------|--------------|--------|-----------|--------------|-------------
| ga01  | 2020-06-11 | Garmin       | VIRB 360    | Timelapse     | TRUE         | [LINK]()        |
| ga02  | 2020-06-11 | Garmin        | VIRB 360    | Video | See notes         | [LINK]()    |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### ga01

```
exiftool -G -s -b -j -a -T V5660909.JPG > garmin_virb_360_V5660909_timelapse_metadata.json
```

#### ga02

Garmin VIRB 360 does not write GPS / telemetry track into the mp4 video file.

The VIRB writes a seperate `.fit` file with GPS telemetry. The attached fit files for the video below are found in 2018-01-11-17-33-54.fit

**Video level data**

```
exiftool -ee -G -s -b -j -a -T V0380038.MP4 > garmin_virb_360_V0380038_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T V0380038.MP4 > garmin_virb_360_V0380038_metadata_track.json
```