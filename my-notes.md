
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
```
