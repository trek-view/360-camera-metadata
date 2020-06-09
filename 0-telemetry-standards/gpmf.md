# GPMF

All GoPro 360 cameras write data in their own GoPro Metadata Format (GPMF / GPMD) also called the General Purpose Metadata Framework.

[This blog post provides a good introduction](https://gopro.com/en/us/news/gopro-video-metadata-open-source-explained).

[A GPMF-parser was recently made available as an open source project](https://github.com/gopro/gpmf-parser). This repo explains the standard in detail.

[The format is also understood by the open-source Exiftool](https://exiftool.org/). [The logic used in exiftool for extraction can be viewed here](https://github.com/exiftool/exiftool/blob/master/lib/Image/ExifTool/GoPro.pm).

[Some of this logic was inspired by this repo too](https://github.com/stilldavid/gopro-utils).

[A new open source repository has been created for the purpose GPMF-Write](https://github.com/gopro/gpmf-write).

One important point to note: `CreateDate` fields in metadata refer to the time the image was stitched. When stitching is done on a PC, the reported `CreateDate` can therefore differ significantly from the actual time the imagery was captured. In many cases it is therefore more accurate to rely on the reported `GPSDateTime` values for true capture times.