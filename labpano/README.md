# Labpano Pilot Metadata

## Labpano Pilot 360 Cameras

1. [Labpano Pilot One](https://www.labpano.com/one)
2. [Labpano Pilot Era](https://pilot.labpano.com/)
3. [Labpano Pilot Lock](https://www.labpano.com/lock)

### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
| lp01  | 2020-06-8  | Labpano  | Pilot Era  | Video  | true (camm6) | [LINK](https://drive.google.com/open?id=11XH0EfdKn_IlrJFCeXD0Qe4ACRiKtKLR)    |
| lp02  | 2020-06-8  | Labpano  | Pilot Era  | Timelapse  | true  | [LINK](https://drive.google.com/file/d/14reAVDK9f_ktRPinHrJelHGnNvFIyBh-/view?usp=sharing)    |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### lp01

**Video level data**

```
exiftool -ee -G -s -b -j -a -T 200207_085206318.mp4 > labpano_pilot_era_200207_085206318_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T 200207_085206318.mp4 > labpano_pilot_era_200207_085206318_metadata_track.json
```

#### lp02

```
exiftool -G -s -b -j -a -T 200207_094350655.jpg > labpano_pilot_era_200207_094350655_timelapse_metadata.json
```