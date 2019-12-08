
Setup notes from https://docs.aws.amazon.com/deeplens/latest/dg/deeplens-headpose-project-prepare-training-data.html


```
virtualenv myproject
source myproject/bin/activate
pip install numpy
pip install opencv-python
```

```
 python preprocessingDataset_py2.py --num-data-aug 15 --aspect-ratio 1
 ```

## Output 
```
$ python preprocessingDataset_py2.py --num-data-aug 15 --aspect-ratio 1
('Number of data augmentation: ', 15)
Aspect Ratio 1:1 (84 pix x 84 pix)
**----  Downloading Dataset  ----**
HeadPoseImageDatabase.tar.gz
**----  Training Data  ----**
0
1
2
3
5
6
7
8
10
11
12
13
0
1
2
3
4
5
6
7
8
9
10
11
12
13
14
(84, 84, 3, 33480)
(33480, 2)
**----  Validation Data  ----**
4
9
14
0
1
2
(84, 84, 3, 1674)
(1674, 2)
((1674, 3, 84, 84), (33480, 3, 84, 84))
((1674, 2), (33480, 2))
('HeadPoseData_trn_test_x15_py2.pkl', ' is saved!')
**----  Done  ----**
$
```

## Copy
```
aws s3 cp HeadPoseData_trn_test_x15_py2.pkl s3://deeplens-sagemaker-models-saubury/headpose/datasets 

```

## Timing
```
Start Dec  7 17:35 
Stop  Dec  8 11:24 HeadPoseData_trn_test_x15_py2.pkl

18 hrs elapsed
```
