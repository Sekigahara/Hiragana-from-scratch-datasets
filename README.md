# Hiragana characters dataset for object detection
The dataset is taken with smartphone camera and annotated with [YoloLabeler](https://github.com/developer0hye/Yolo_Label).</br>
This repository also linked with different project of Japanese recognition with YOLOv4, find the detail of the repository [here](https://github.com/Sekigahara/ETL-extractor-YOLOv4).

## Dataset characteristic

### Writing variety
- Written in various arrangement(Written in pencil, pen, vertically oriented, different size and randomly in one set)
- Each character set is written in 3 different paper, each character is written 20 times.

### Picture taking
- For each paper the picture will be taken in 5 different take.
- Taken in 4 different angle(above, right, left and bottom)
- The last is taken from above with phone camera flashes.

### Data arrangement
- In folder dataset, the data is grouped based on the first romaji consonant except the first hiragana set which is ```(あ-a to お-o)```
- For each folders are filled with the same consonant with different vocal pronounce. For example in folder ```Ka``` will be consisting character of ```(か-ka to こ-ko)```.
- The total label is 46.
- The total of the pictures are 300 files within 10 folders.

## Scripts
- The first script is augmentation.ipynb, perform brightness augmentation in different range and copy the annotated coordinates and perform data split. In this script, it's really possible to add more augmentation technique especially photomeric distortion that did not changes the object preposition.
- The second script is train_txt_formatter.ipynb, this script list every pictures and add it to the train.txt and test.txt for YOLOv4 Darknet training by [AlexeyAB](https://github.com/AlexeyAB/darknet).
