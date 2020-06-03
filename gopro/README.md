# GoPro Metadata

## GoPro 360 Cameras

GoPro offer two models of 360 cameras:

1. [GoPro Fusion (discontiuned)](/gopro/fusion/README.md)
2. [GoPro MAX](/gopro/max/README.md)

### Photo metadata

Photos use a standard mix of EXIF and XMP metadata.

### Video metadata

All GoPro 360 cameras write data in their own GoPro Metadata Format (GPMF / GPMD) also called the General Purpose Metadata Framework.

[This blog post provides a good introduction](https://gopro.com/en/us/news/gopro-video-metadata-open-source-explained).

[A GPMF-parser was recently made available as an open source project](https://github.com/gopro/gpmf-parser). This repo explains the standard in detail.

[The format is also understood by the open-source Exiftool](https://exiftool.org/).

[A new open source repository has been created for the purpose GPMF-Write](https://github.com/gopro/gpmf-write).