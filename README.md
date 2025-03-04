# CMS
## Run CMS:

```./cms.py --building-dataset [building dataset file] --car-dataset [car dataset file]```

### Building dataset format

Building power consumption readings (kW) separated by new lines.

First reading is reading at 6pm. Each reading is two seconds apart. 

### Car dataset format

List of cars separated by new lines.

Format of each line: name, arrival time (seconds), departure time (hh:mm:ss), model, desired change in SoC (%), sleep mode (True/False).

Arrival time of 0 means the car arrives at 6pm.

### Examples

See building_datasets and car_datasets for correct dataset format.

## Run visualization interface:

```./cms.py --building-dataset [building dataset file] --car-dataset [car dataset file] --visualization-port 9000```

```./visualization.py 9000```

## Connect to OpenEVSE and Zeka via CAN:

```./cms.py --building-dataset [building dataset file] --car-dataset [car dataset file] --user-input-port 8000 --openevse-port /dev/ttyUSB0 --zeka-port /dev/cu.usbmodem14101```

```./user_input.py 8000```

## Run fast sim:

```./cms.py --building-dataset [building dataset file] --car-dataset [car dataset file] --fast-sim```

## Log each car's data (logs will show in logs folder):

Car format: measured current, advertised current, battery current, SoC, battery's station number

Station format: discharge current, charge current, battery capacity

```./cms.py --building-dataset [building dataset file] --car-dataset [car dataset file] --log```

## Help:

```./cms.py --help```
