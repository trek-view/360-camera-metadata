# Ricoh Metadata

## Ricoh 360 Cameras

1. Theta V1

### Photo metadata


### Video metadata research


### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### VIDEO

**Video level data**

```
exiftool -ee -G -s -b -j -a -T VIDEO.mp4 > MANUFACTURER_MAKE_VIDEO_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T VIDEO.mp4 > MANUFACTURER_MAKE_VIDEO_metadata_track.json
```

#### IMAGE

```
exiftool -G -s -b -j -a -T IMAGE.jpg > MANUFACTURER_MAKE_IMAGE_timelapse_metadata.json
```