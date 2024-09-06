# Human3.6M Dataset

Just need to download the dataset from the Google Drive link and extract:

https://drive.google.com/file/d/1dzuIWfNBxvIFHPdB7_JLiwALYNKeZHtV/view?usp=drive_link




## Unalinged dataset

download and unzip the dataset:
the original Human3.6m dataset.

The original dataset is large and it needs edu email and need check and get permission for downloading.

The simple way is to directly download it:

```
wget http://visiondata.cis.upenn.edu/volumetric/h36m/h36m_annot.tar
tar -xf h36m_annot.tar
rm h36m_annot.tar

# Download H36M images
mkdir -p h36m/images
cd h36m/images
wget http://visiondata.cis.upenn.edu/volumetric/h36m/S1.tar
tar -xf S1.tar
rm S1.tar
wget http://visiondata.cis.upenn.edu/volumetric/h36m/S5.tar
tar -xf S5.tar
...
S6, S7, S8, S9, S11
```


move_data.sh:
```
target=S9
mkdir ${target}
mv ${target}_Directions* ${target}/
mv ${target}_Discussion* ${target}/
mv ${target}_Posing* ${target}/
mv ${target}_Waiting* ${target}/
mv ${target}_Greeting* ${target}/
mv ${target}_Walking* ${target}/
```

## Background


After these steps, I found it lacks landmarks annotations and I can't run the code.

Then I found that The project doesn't use the original Human3.6m dataset.

It uses the dataset from the following link:

https://github.com/YutingZhang/lmdis-rep

The lmdis-rep project provides a simplfied dataset, which can be downloaded from the Google Drive I provided at the beginning.
