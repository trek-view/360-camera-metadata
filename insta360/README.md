# Insta360 Metadata

## Insta360 360 Cameras

1. [ONE](https://www.insta360.com/product/insta360-one/)
2. [ONE X](https://www.insta360.com/product/insta360-onex/)
3. [ONE R](https://www.insta360.com/product/insta360-oner_1inch-edition)
4. [Pro](https://www.insta360.com/product/insta360-pro/)
5. [Pro2](https://www.insta360.com/product/insta360-pro2/)
6. [Titan](https://www.insta360.com/product/insta360-titan/)

### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
| is01  | 2020-06-08  | insta360  | pro2  | video  | true  | [LINK](https://drive.google.com/file/d/136CruQHa0Pg74QiREM4k52nbR1FCsVjU/view?usp=sharing)  |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### is01

**Video level data**

```
exiftool -ee -G -s -b -j -a -T insta-pro2-002.mp4 > insta360_pro2_insta-pro2-002_metadata_overview.json
```

**Track level data (more verbose -- includes telemetry)**

```
exiftool -ee -G3 -s -b -j -a -T insta-pro2-002.mp4 > insta360_pro2_insta-pro2-002_metadata_track.json
```
