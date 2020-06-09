# Samsung Metadata

## Samsung 360 Cameras

1. [Gear 360](https://www.samsung.com/uk/support/model/SM-R210NZWABTU/)

### Metadata DB

| id  | data_added  | manufacturer  | model  | type  | is_geotagged_by_cam  | sample_file  |
|---|---|---|---|---|---|---|
| sa01  | 2020-06-10  | Samsung  | Gear 360  | Timelapse  | true  | [LINK](https://drive.google.com/file/d/11cnuC-8kiLeHK5PlvRik56Gzy_bcfDCO/view?usp=sharing)    |
|   |   |   |   |   |   |   |
|   |   |   |   |   |   |   |

_Note: camera firmware update might alter the metadata produced by the camera. The latest firmware was used on when the sample file was taken and date uploaded (`data_added`)._

### Note on how data was extracted

#### sa01

```
exiftool -G -s -b -j -a -T AEML5317.JPG > samsung_gear_360_AEML5317_timelapse_metadata.json
```