# GoPro Metadata

## GoPro 360 Cameras

GoPro offer two models of 360 cameras:

1. GoPro Fusion (discontiuned)
2. GoPro MAX

### Photo metadata



### Video metadata reseach

All GoPro 360 cameras write data in their own GoPro Metadata Format (GPMF / GPMD) also called the General Purpose Metadata Framework.

[This blog post provides a good introduction](https://gopro.com/en/us/news/gopro-video-metadata-open-source-explained).

[A GPMF-parser was recently made available as an open source project](https://github.com/gopro/gpmf-parser). This repo explains the standard in detail.

[The format is also understood by the open-source Exiftool](https://exiftool.org/). [The logic used in exiftool for extraction can be viewed here](https://github.com/exiftool/exiftool/blob/master/lib/Image/ExifTool/GoPro.pm).

[Some of this logic was inspired by this repo too](https://github.com/stilldavid/gopro-utils).

[A new open source repository has been created for the purpose GPMF-Write](https://github.com/gopro/gpmf-write).

### Metadata DB

| id   | data_added | manufacturer | model  | type      | is_geotagged | sample_file | metadata_output |
|------|------------|--------------|--------|-----------|--------------|-------------|-----------------|
| gp01  | 2020-05-03 | GoPro        | Max    | Video     | TRUE         | [LINK](https://drive.google.com/file/d/10DTo7gfmyO3SO0KXpypSOMn_-iRqZp9Z/view?usp=sharing)    | [LINK](/gopro/gopro_max_GS012804_video_metadata.txt)        |
| gp02  | 2020-05-03 | GoPro        | Max    | Timelapse | TRUE         | [LINK](https://drive.google.com/drive/u/1/folders/1PKPiozKat7TLZgOcOTy6CVs1_P2EVwWO)    | [LINK](/gopro/gopro_max_GSAG2002_timelapse_metadata.txt)        |
| gp03  | 2020-05-03 | GoPro        | Fusion | Video     | TRUE         | [LINK](https://drive.google.com/file/d/1r9ztRU6nTGnPk3NRANd1FTZionQUdqo7/view?usp=sharing)    | [LINK](/gopro/gopro_fusion_VIDEO_7152_metadata.txt)        |
| gp04  | 2020-05-03 | GoPro        | Fusion | Timelapse | TRUE         | [LINK](https://drive.google.com/drive/u/1/folders/1fDYbUN2y62ZUa09lOLBJjUpmKFNf6r31)    | [LINK](/gopro/gopro_fusion_MULTISHOT_0611_000000_timelapse_metadata.txt)        |
|       |            |              |        |           |              |             |                 |

### Note on how we extracted data

**gp01**

```
exiftool -ee -G3 -s GS012804.mp4 > gopro_max_GS012804_video_metadata.txt
```

**gp02**

```
exiftool -G -a -s GSAG2002.JPG > gopro_max_GSAG2002_timelapse_metadata.txt
```

**gp03**

```
exiftool -ee -G3 -s VIDEO_7152.mp4 > gopro_fusion_VIDEO_7152_metadata.txt
```

**gp04**

```
exiftool -G -a -s MULTISHOT_0611_000000.jpg > gopro_fusion_MULTISHOT_0611_000000_timelapse_metadata.txt
```