# GoPro Metadata

## GoPro 360 Cameras

1. [GoPro Fusion (discontinued)](https://gopro.com/en/us/fusion)
2. [GoPro MAX](https://gopro.com/en/us/shop/cameras/max/CHDHZ-201-master.html)

### Metadata DB

| id   | data_added | manufacturer | model  | type      | is_geotagged_by_cam | sample_file |
|------|------------|--------------|--------|-----------|--------------|-------------
| gp01  | 2020-05-03 | GoPro       | Max    | Video     | TRUE         | [LINK]()        |
| gp02  | 2020-05-03 | GoPro       | Max    | Timelapse | TRUE         | [LINK](https://drive.google.com/drive/u/1/folders/1PKPiozKat7TLZgOcOTy6CVs1_P2EVwWO)    |
| gp03  | 2020-05-03 | GoPro       | Fusion | Video     | TRUE         | [LINK](https://drive.google.com/file/d/1r9ztRU6nTGnPk3NRANd1FTZionQUdqo7/view?usp=sharing)    |
| gp04  | 2020-05-03 | GoPro       | Fusion | Timelapse | TRUE         | [LINK](https://drive.google.com/drive/u/1/folders/1fDYbUN2y62ZUa09lOLBJjUpmKFNf6r31)    |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### gp01

**Video level data**

```
exiftool -ee -G -s -b -j -a -T GS012804.mp4 > gopro_max_GS012804_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T GS012804.mp4 > gopro_max_GS012804_metadata_track.json
```

#### gp02

```
exiftool -G -s -b -j -a -T GSAG2002.jpg > gopro_max_GSAG2002_timelapse_metadata.json
```

#### gp03

**Video level data**

```
exiftool -ee -G -s -b -j -a -T VIDEO_7152.mp4 > gopro_fusion_VIDEO_7152_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T VIDEO_7152.mp4 > gopro_fusion_VIDEO_7152_metadata_track.json
```

#### gp04

```
exiftool -G -s -b -j -a -T MULTISHOT_0611_000000.jpg > gopro_fusion_MULTISHOT_0611_000000_timelapse_metadata.json
```