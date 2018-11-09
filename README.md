# celeba-hq-modified

![imga](https://raw.githubusercontent.com/willylulu/celeba-hq-modified/master/0.jpg)

A modified approach to generate __CelebA-HQ Dataset__

The CelebA-HQ is a dataset introduced in _Progressive Growing of GANs for Improved Quality_ ([progressive_growing_of_gans](https://github.com/tkarras/progressive_growing_of_gans)), containing 30,000 high quality images from CelebA.

The images are originally stored as _HDF5 format (.h5)_, which are not suitable for common data loaders. Therefore, I modified the `h5tool.py` to generate and save CelebA-HQ images in _JPEG format (.jpg)_.


## Usage

1.	Clone the original repository

`git clone https://github.com/tkarras/progressive_growing_of_gans/tree/original-theano-version`

2.	Clone this repository

`git clone https://github.com/willylulu/celeb-hq-modified`

3.	Replace `h5tool.py` in the original repo with the one in this repo

`cp celeb-hq-modified/h5tool.py progressive_growing_of_gans/h5tool`

4.	Create target directory in the original repository

```
cd progressive_growing_of_gans
mkdir celeba-hq
cd celeba-hq
mkdir celeba-64
mkdir celeba-128
mkdir celeba-256
mkdir celeba-512
mkdir celeba-1024
```

5.	Go back to home path

`cd`

6.	Create a directory B and download [CelebA **non-aligned version**](https://drive.google.com/open?id=0B7EVK8r0v71peklHb0pGdDl6R28) and put them in directory A

7.	Create a directory A and download [CelebA-HQ zip file](https://drive.google.com/drive/folders/0B4qLcYyJmiz0TXY1NG02bzZVRGs) and put them in directory B

8.	Download [annotation files](https://drive.google.com/open?id=0B7EVK8r0v71pOC0wOVZlQnFfaGs) and put them in directory B
9.	Execute `h5tool.py`
`python h5tool.py create_celeba_hq 123456.h5 <path to directory A> <path to directory B>`

##	Reference
[tkarras/progressive_growing_of_gans](https://github.com/tkarras/progressive_growing_of_gans)

[CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
