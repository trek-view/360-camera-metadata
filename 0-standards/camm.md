# CAMM (Camera Motion Metadata Spec)

[Google has created a comprehensive page detailing the `CAMM` data format you will find useful in understanding the decoded structure and content](https://developers.google.com/streetview/publish/camm-spec#data-format).

In short there should be only one CAMM track per MP4 video file.

[Within the CAMM track there are 7 cases (think of them as layers)](https://developers.google.com/streetview/publish/camm-spec#data-format).

The video does not write to all layers (because some cases have duplicate fields (e.g. camm5 and camm6 both have latitude and longitude fields).

## Deconstructing the CAMM Spec

### camm

**Description:**

The video file should contain the following sample entry box to indicate the custom metadata track, and the subComponentType of the track should be set to meta.

**Structure:**

```
Camera Motion Metadata Sample Entry (camm)

Definition
Box Type: camm
Container: stsd
A sample entry indicating the data track that saves the camera motion.

Syntax
aligned(8) class CameraMotionMetadataSampleEntry extends SampleEntry('camm') {
}
  
```
**Example:**

```
  "Main:HandlerDescription": {
    "id": 24,
    "table": "QuickTime::Handler",
    "val": "CameraMetadataMotionHandler"
  },
  "Main:OtherFormat": {
    "id": 4,
    "table": "QuickTime::OtherSampleDesc",
    "val": "camm"
  }
```

_Taken from: Insta360 Pro2_

### camm0

**Description:**

Angle axis orientation in radians representing the rotation from local camera coordinates to a world coordinate system. The world coordinate system is defined by applications.

**Structure:**

```
  case 0:
    float angle_axis[3];
  break;
```

**Example:**

```

```

### camm1

**Description:**



**Structure:**

```
  case 1:
    int32 pixel_exposure_time;
    int32 rolling_shutter_skew_time;
  break;
```

**Example:**

```

```

### camm2

**Description:**

**Structure:**

```
  case 2:
    float gyro[3];
  break;
```

**Example:**

```
  "Doc1:AngularVelocity": {
    "id": 4,
    "table": "QuickTime::camm2",
    "val": "0.0462660863995552 0.139929175376892 -0.204053655266762"
  }
```

_Taken from: Insta360 Pro2_

### camm3

**Structure:**

```
  case 3:
    float acceleration[3];
  break;
```

**Example:**

```
  "Doc2:Acceleration": {
    "id": 4,
    "table": "QuickTime::camm3",
    "val": "1.1484375 -0.0741699188947678 15.0469236373901"
  }
```

_Taken from: Insta360 Pro2_

### camm4

**Structure:**

```
  case 4:
    float position[3];
  break;
```

**Example:**

```

```

### camm5

**Structure:**

```
  case 5:
    double latitude;
    double longitude;
    double altitude;
  break;
```

**Example:**

```

```

### camm6

**Structure:**

```
  case 6:
    double time_gps_epoch;
    int gps_fix_type;
    double latitude;
    double longitude;
    float altitude;
    float horizontal_accuracy;
    float vertical_accuracy;
    float velocity_east;
    float velocity_north;
    float velocity_up;
    float speed_accuracy;
  break;
```

**Example:**

```
  "Doc25:GPSDateTime": {
    "id": 4,
    "table": "QuickTime::camm6",
    "val": "2020:04:02 09:43:22.2Z"
  },
  "Doc25:GPSMeasureMode": {
    "id": 12,
    "table": "QuickTime::camm6",
    "val": "3-Dimensional Measurement"
  },
  "Doc25:GPSLatitude": {
    "id": 16,
    "table": "QuickTime::camm6",
    "val": "50.456102 N"
  },
  "Doc25:GPSLongitude": {
    "id": 24,
    "table": "QuickTime::camm6",
    "val": "30.479831 E"
  },
  "Doc25:GPSAltitude": {
    "id": 32,
    "table": "QuickTime::camm6",
    "val": "146.8 m"
  },
  "Doc25:GPSHorizontalAccuracy": {
    "id": 36,
    "table": "QuickTime::camm6",
    "val": 1.02999997138977
  },
  "Doc25:GPSVerticalAccuracy": {
    "id": 40,
    "table": "QuickTime::camm6",
    "val": 1.02999997138977
  },
  "Doc25:GPSVelocityEast": {
    "id": 44,
    "table": "QuickTime::camm6",
    "val": 0.699336230754852
  },
  "Doc25:GPSVelocityNorth": {
    "id": 48,
    "table": "QuickTime::camm6",
    "val": 1.19965398311615
  },
  "Doc25:GPSVelocityUp": {
    "id": 52,
    "table": "QuickTime::camm6",
    "val": 0
  },
  "Doc25:GPSSpeedAccuracy": {
    "id": 56,
    "table": "QuickTime::camm6",
    "val": 0
  },
```

_Taken from: Insta360 Pro2_

### camm7

**Structure:**

```
  case 7:
    float magnetic_field[3];
  break;
```

**Example:**

```

```