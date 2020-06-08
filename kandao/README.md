# Kandao Metadata

## Kandao 360 Cameras

https://www.kandaovr.com/

1. QooCam
2. QooCam 8k
3. Obsidian GO
4. Obsidian S & R

### Photo metadata

Any relevant docs, blogs, manuals...

### Video metadata research

Any relevant docs, blogs, manuals...


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