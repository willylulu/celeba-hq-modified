# celeba-hq-modified
A modified approach getting celeb-hq dataset

Replace saving in h5 file system with directly storing in picture
##	Usage
1.	Clone original repo

`git clone https://github.com/tkarras/progressive_growing_of_gans/tree/original-theano-version`

2.	Clone this repo

`git clone https://github.com/willylulu/celeb-hq-modified`

3.	Replace h5tool.py file in original repo with this repo

`cp celeb-hq-modified/h5tool.py progressive_growing_of_gans/h5tool`

4.	Create target directory in progressive_growing_of_gans repo

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

5.	Back to home path
`cd`
6.	Create a directory A and [download celeb-hq zip file](https://drive.google.com/drive/folders/0B4qLcYyJmiz0TXY1NG02bzZVRGs) and put them in directory A
7.	Creare a directory B and [download celebA **not align version**](https://drive.google.com/open?id=0B7EVK8r0v71peklHb0pGdDl6R28) and put them in directory B
8.	[Downloadd anno file](https://drive.google.com/open?id=0B7EVK8r0v71pOC0wOVZlQnFfaGs) and put them in directory B
9.	Excute h5tool.py
`python h5tool.py create_celeba_hq 123456.h5 <path to directory A> <path to directory B>`

##	Reference
[tkarras/progressive_growing_of_gans](https://github.com/tkarras/progressive_growing_of_gans)

[CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html)
