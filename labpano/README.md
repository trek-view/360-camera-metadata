# Labpano Pilot Metadata

## Labpano Pilot 360 Cameras

1. [Labpano Pilot One](https://www.labpano.com/one)
2. [Labpano Pilot Era](https://pilot.labpano.com/)
3. [Labpano Pilot Lock](https://www.labpano.com/lock)

### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | geotagged_by_cam  |
|---|---|---|---|---|---|
| lp01  | 2020-06-08  | Labpano  | Pilot Era  | Video  | requires_module (camm6) |
| lp02  | 2020-06-08  | Labpano  | Pilot Era  | Timelapse  | requires_module |
| lp03  | 2020-06-20  | Labpano  | Pilot One  | Video  | requires_module (camm6) |
| lp04  | 2020-06-20 | Labpano  | Pilot One  | Timelapse  | requires_module  |

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

#### lp03

**Video level data**

```
exiftool -ee -G -s -b -j -a -T 200619_161801314.mp4 > labpano_pilot_one_200619_161801314_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T 200619_161801314.mp4 > labpano_pilot_one_200619_161801314_metadata_track.json
```

#### lp04

```
exiftool -G -s -b -j -a -T 200619_161719613.jpg > labpano_pilot_one_200619_161719613_timelapse_metadata.json
```