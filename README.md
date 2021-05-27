# Youtube Trends Analytics Inoxoft-Bootcamp-Project

Pet-project developed during [Inoxoft](https://inoxoft.com/) [Data-Focused Programming Bootcamp](https://inoxoft.com/course/data-focused-programming/) [2021](https://dou.ua/calendar/37008/) </br> </br>

## Project description </br>

### Project tasks:

1. What makes a Youtube video (or/and channel) more popular when compared to others?
2. Do there exist any underlying factors which affect the popularity of a video (or/and channel) on Youtube?
3. Could we, and if so, how adjust the video parameters to make it more popular?

Wish us the best of luck on our journey! </br>

### Data-resources:

1. https://www.kaggle.com/harshithgupta/youtubes-channels-dataset

2. https://www.kaggle.com/jyotmakadiya/top-trending-videos-youtube-2021 </br>

### Data overview:

The datasets contain a total of 41 columns from two datasets describing interesting features such as Title, date/time of upload, description of video.

Currently, the first one contains data from 10 Regions/Countries scrapped from Google YouTube API. The second dataset is a daily record of the top trending YouTube videos. </br>

### Project team

In alphabetical order:

- [Danylo Ivanchyshyn](https://github.com/DanyloIvanchyshyn)
- [Elena Matusova](https://github.com/ElenaMatusova)
- [Volodymyr Zalevskyi](https://github.com/zalevskyi) </br>

### Project structure

#### Install

docker files for various use cases:

- GPU Training (Mac/Linux only)
- CPU Training
- Deployment (intended to be as lightweight as possible)

To build images you can run scripts in `./utils` </br>

#### Data

Data downloaders, athena queries etc..
To run docker shell you can use scripts in `./utils`

```
python -i data/url_to_category/download_tools.py
```

#### Train

Model examples for training (and exporting models)
To run docker jupyter-notebook you can use scripts in `./utils`

```
#go to train folder and open the notebook
```

or

```
#run automated hyperparameter searcher using hyperas
python train/example_AUTO.py
```

NOTE: it'll be useful to keep track of system resources while training, try `nvidia-smi` for GPU, `nload` for network, and `htop` for CPU. </br>

#### Deploy

a home for deployable models and test scripts </br>

#### Utils

General purpose scripts (running a shell inside docker quickly etc...) </br>

##### Mac/Linux

- To build a docker image: `source utils/builddocker.sh minimal.Dockerfile`
- To run shell of a docker image: `source utils/runshell.sh`
- To run jupyter-notebook of a docker image: `source utils/runnotebook.sh` </br>

##### Windows

using powershell

- To build a docker image: `./utils/builddocker.ps1`
- To run shell of a docker image: `./utils/runshell.ps1`
- To run jupyter-notebook of a docker image: `./utils/runnotebook.ps1` </br>
