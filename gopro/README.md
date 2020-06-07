# GoPro Metadata

## GoPro 360 Cameras

GoPro offer two models of 360 cameras:

1. GoPro Fusion (discontinued)
2. GoPro MAX

### Photo metadata



### Video metadata research

All GoPro 360 cameras write data in their own GoPro Metadata Format (GPMF / GPMD) also called the General Purpose Metadata Framework.

[This blog post provides a good introduction](https://gopro.com/en/us/news/gopro-video-metadata-open-source-explained).

[A GPMF-parser was recently made available as an open source project](https://github.com/gopro/gpmf-parser). This repo explains the standard in detail.

[The format is also understood by the open-source Exiftool](https://exiftool.org/). [The logic used in exiftool for extraction can be viewed here](https://github.com/exiftool/exiftool/blob/master/lib/Image/ExifTool/GoPro.pm).

[Some of this logic was inspired by this repo too](https://github.com/stilldavid/gopro-utils).

[A new open source repository has been created for the purpose GPMF-Write](https://github.com/gopro/gpmf-write).

One important point to note: `CreateDate` fields in metadata refer to the time the image was stitched. When stitching is done on a PC, the reported `CreateDate` can therefore differ significantly from the actual time the imagery was captured. In many cases it is therefore more accurate to rely on the reported `GPSDateTime` values for true capture times.

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