# Ricoh Metadata

## Ricoh 360 Cameras

1. [Theta V](https://theta360.com/en/about/theta/v.html)
2. [Theta Z1](https://theta360.com/en/about/theta/z1.html)

### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
| th01  | 2020-06-07  | Ricoh  | Theta V  | timelapse  | smartphone  | [LINK](https://drive.google.com/file/d/1_l1CxBeTv1Qp8u58QWQq3Bckgy2S_kgW/view?usp=sharing)   |
| th02  | 2020-06-07  | Ricoh  | Theta V  | video  | smartphone  | [LINK](https://drive.google.com/file/d/1-izVfxpsyrj7-Yz3-dziZ_QRmgWBYlaB/view?usp=sharing)   |
| th03  | 2020-06-07  | Ricoh  | Theta Z1  | timelapse  | smartphone  | [LINK](https://drive.google.com/open?id=14mvsO5b--XJvtyzkeGp7dmribRNGkloT)   |
| th04  | 2020-06-07  | Ricoh  | Theta Z1  | video  | smartphone  | [LINK](https://drive.google.com/open?id=1MsLyahfjbDZTXRBgSBVo22UcHe5X1miwT)

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### Video file notes

Seems that both the Theta V and Z1 only include camm2 and camm3 in the camm track -- no GPS telemetry (camm5 / camm6).

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

#### th03

```
exiftool -G -s -b -j -a -T R0013798.JPG > theta_z1_R0013798_timelapse_metadata.json
```

#### th04

**Video level data**

```
exiftool -ee -G -s -b -j -a -T R008000.MP4 > theta_z1_R008000_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T R008000.MP4 > theta_z1_R008000_metadata_track.json
```