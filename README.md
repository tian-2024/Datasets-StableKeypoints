# Datasets for StableKeypoints

User guide of the 5 datasets used in [StableKeypoints](https://github.com/ubc-vision/StableKeypoints):
1. [CelebA](1-celeba)
2. [CUB](2-cub)
3. [DeepFashion](3-deepfashion)
4. [Taichi](4-taichi)
5. [Human3.6m](5-human36m)


## Background

Recently, I came across an intriguing project called StableKeypoints, which was published at CVPR 2024.

I attempted to run the project using its dataset but encountered some issues with almost every dataset.

After searching for solutions on the website and experimenting with the code, I managed to resolve most of these problems.

To make it more convenient for myself and others in the future, I am compiling some useful resources here.


## Time Consuming for optimization embedding of 500 steps


Different datasets almost have the same time consuming for optimization embedding.
Because the iteration numbers is `num_steps * (batch_size // num_gpus)`, which means the dataset size doesn't affect the iteration numbers.

The default batch_size is 4, so num_gpus must less than or equal to 4.
Commonly, num_gpus is 4, so the total iterations are `num_steps * 4 // 4 = num_steps`.
num_steps default is 500.

In practical experiments, the time consuming for optimization embedding about 20~30 minutes, affected by the status of the gpu (busy or idle).

- celeba: 19 minutes
- cub: 31 minutes
- deepfashion: 19 minutes
- human36m: 20 minutes
- taichi: 32 minutes


## dataset size

| Dataset             | Train  | Test  |
| ------------------- | ------ | ----- |
| taichi              | 5000   | 300   |
| cub_aligned         | 5964   | 2874  |
| cub_001             | 29     | 17    |
| cub_002             | 30     | 14    |
| cub_003             | 30     | 15    |
| cub_all             | 5964   | 2874  |
| deepfashion         | 10604  | 1179  |
| celeba_aligned      | 19000  | 1000  |
| celeba_wild         | 5379   | 283   |
| human3.6m           | 796648 | 87975 |
| unaligned_human3.6m | 159444 | 17615 |


## Time Consuming for Precomputing keypoints

The iteration depends on min(len(dataset), max_num_points).

The dataset here means the	training set.
And max_num_points is 50000.

Different datasets have different sizes, so the iteration numbers may vary.

| Dataset     | Time      | Images                   |
| ----------- | --------- | ------------------------ |
| taichi      | 2 hours   | 5000                     |
| cub         | 4 hours   | 5964                     |
| deepfashion | 7 hours   | 10604                    |
| celeba      | 9.3 hours | 19000                    |
| human36m    | 22 hours  | 50000  (actually 796648) |


## Time Consuming for evaluating

The iteration is exactly on len(test dataset).

So it will totally depends on the size of the test dataset.

| Dataset     | Time      | Images |
| ----------- | --------- | ------ |
| taichi      | 0.1 hours | 300    |
| celeba      | 0.5 hours | 1000   |
| deepfashion | 1 hour    | 1179   |
| cub         | 2 hours   | 2874   |
| human36m    | -         | 87975  |
