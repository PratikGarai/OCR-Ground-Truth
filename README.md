# A simple Ground Truth File demo and example for OCR tasks

## Image included

| Image         |     Class      |          Class (Case Preserved) |
| ---         |     ---      |          --- |
| <img src="./images/demo_1.png" width="300">    |   available   |  Available   |
| <img src="./images/demo_2.jpg" width="300">      |    shakeshack    |   SHARESHACK    |
| <img src="./images/demo_3.png" width="300">  |   london   |  Londen   |
| <img src="./images/demo_4.png" width="300">      |    greenstead    |   Greenstead    |
| <img src="./images/demo_5.png" width="300" height="100">    |   toast   |  TOAST   |
| <img src="./images/demo_6.png" width="300" height="100">      |    merry    |   MERRY    |
| <img src="./images/demo_7.png" width="300">    |   underground   |   underground  |
| <img src="./images/demo_8.jpg" width="300">      |    ronaldo    |    RONALDO   |
| <img src="./images/demo_9.jpg" width="300" height="100">    |   bally   |   BALLY  |
| <img src="./images/demo_10.jpg" width="300" height="100">      |    university    |   UNIVERSITY    |


## Steps to create

1. Create your own lmdb dataset.
```
pip3 install fire
python3 create_lmdb_dataset.py --inputPath data/ --gtFile data/gt.txt --outputPath result/
```
The structure of data folder as below.
```
data
├── gt.txt
└── test
    ├── word_1.png
    ├── word_2.png
    ├── word_3.png
    └── ...
```
At this time, `gt.txt` should be `{imagepath}\t{label}\n` <br>
For example
```
test/word_1.png Tiredness
test/word_2.png kills
test/word_3.png A
...
```