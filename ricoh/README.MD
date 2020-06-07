# Ricoh Metadata

## Ricoh 360 Cameras

1. Theta V

### Photo metadata


### Video metadata research


### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
| th01  | 2020-06-07  | Ricoh  | Theta V  | timelapse  | smartphone  | [LINK](https://drive.google.com/file/d/1_l1CxBeTv1Qp8u58QWQq3Bckgy2S_kgW/view?usp=sharing)   |
| th02  | 2020-06-07  | Ricoh  | Theta V  | video  | smartphone  | [LINK](https://drive.google.com/file/d/1-izVfxpsyrj7-Yz3-dziZ_QRmgWBYlaB/view?usp=sharing)   |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### th01

```
exiftool -G -s -b -j -a -T R0014760.jpg > theta_v_R0014760_timelapse_metadata.json
```

#### th02

**Video level data**

```
exiftool -ee -G -s -b -j -a -T 20200511_113008_255.mp4 > theta_v_20200511_113008_255_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T 20200511_113008_255.mp4 > theta_v_20200511_113008_255_metadata_track.json
```


