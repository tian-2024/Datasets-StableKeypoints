# Human3.6M Dataset

The project doesn't use the original Human3.6m dataset.

It uses the simplfied dataset, which can be downloaded from the Google Drive following link:

https://drive.google.com/file/d/1dzuIWfNBxvIFHPdB7_JLiwALYNKeZHtV/view?usp=drive_link



## Original Human3.6m Dataset

Firstly, I downloaded the original Human3.6m dataset, but found it lacks landmarks annotations.

And the original dataset is too large, which is not convenient for downloading and using.

It needs edu email and need check and get permission.

The recommended way is to directly download it:

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
