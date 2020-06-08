# Labpano Pilot Metadata

## Labpano Pilot 360 Cameras

1. Labpano Pilot One
2. Labpano Pilot Era
3. Labpano Pilot Lock

### Photo metadata

Any relevant docs, blogs, manuals...

### Video metadata research

Any relevant docs, blogs, manuals...


### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
| pi01  | 2020-06-8  | Labpano  | Pilot One  | Video  | true  | [LINK]()    |
| pi02  | 2020-06-8  | Labpano  | Pilot One  | Timelapse  | true  | [LINK]()    |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### pi01

**Video level data**

```
exiftool -ee -G -s -b -j -a -T 200207_085206318.mp4 > labpano_pilot_era_200207_085206318_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T 200207_085206318.mp4 > labpano_pilot_era_200207_085206318_metadata_track.json
```

#### pi02

```
exiftool -G -s -b -j -a -T 200207_094350655.jpg > labpano_pilot_era_200207_094350655_timelapse_metadata.json
```