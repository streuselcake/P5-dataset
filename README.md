# Recognizing Running Movement Changes with Quaternions on a Sports Watch - Dataset

This auxiliary dataset can be used to reproduce the findings from our paper (to appear).

Annotated in this dataset are the movement peaks. The file at-gestures.csv contains annotations of the data files. One data file is referenced per lines in the annotation file and the annotations start at the column "earliest visible exageration peak".

All data files in this dataset correspond to a trial with a participant and movement type performed while running. Each data file contains sensor readings and other log outputs. The imuUpdate()-lines in the data are formatted as follows and other log messages are excluded from the data files. The column numbers start at 0 and are described in the following. 

Columns | Data fields
--- | ------
0 | "imuUpdate()"
1 | Addr
2 | Timestamp
3 | DataNr
4-7 | q
8-11 | //intermediate calculation
12-15 | //intermediate calculation
16-19 | a
20-23 | b
24-27 | //intermediate calculation
28-31 | //intermediate calculation
32-35 | aOriginal
36-39 | qAIni
40-43 | qATare
44-47 | bOriginal
48-51 | bIni
52-55 | bTare
56 | aSensorAccuracy
57 | bSensorAccuracy

Quaternion fields expand to four columns corresponding to the quaternion components w, x, y, and z. The quaternions used in the paper are obtained with columns q (4-7), a (16-19), and b (20-23). The original sensor values are obtained with aOriginal and bOriginal. The quaternions qAIni and qTare can be used to account for the global and sensor-to-segment offsets respectively, resulting in a, b, and q as described in the paper.
