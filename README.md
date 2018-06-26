# Data Science For Good: DonorsChoose.org
## Help DonorsChoose.org connect donors with projects they care about

DonorsChoose.org is an organization that helps teachers fundraise for American classrooms. The organization has funded over 1.1 million classroom requests through the support of 3 million donors, the majority of whom were making their first-ever donation to a public school. If DonorsChoose.org can motivate even a fraction of those donors to make another donation, that could have a huge impact on the number of classroom requests fulfilled.  The goal of the project is to enable DonorsChoose.org to build targeted email campaigns in order to recommend specific classroom requests to prior donors. 

The organization has supplied anonymized [data](https://www.kaggle.com/donorschoose/io) regarding donations from the past five years, starting from January 2013 to May 1, 2018.  Six data files are provided with the following dimensions:
* donations (4687884, 10)
* donors (2122640, 5)
* projects (1110017, 15)
* resources (7210448, 4)
* schools (72993, 9)
* teachers (402900, 3)

To solve the problem, three Jupyter Notebooks are created.   Part 1 of the notebooks focuses on Feature Engineering, Part 2 focuses on Data Exploration, and Part 3 focuss on building the recommender system and evaluating the model.  

The recommendation algorithm is based on a combination of Filtering and Ranking.  

In [Part 1](https://nbviewer.jupyter.org/github/kikimeow/DonorsChoose-Recommender-System/blob/master/DonorsChoose-%20Part%201.%20Preprocessing%20%26%20Feature%20Engineering.ipynb) of the notebooks, features are generated to capture the characteristics regarding the donors, the schools, as well as the projects. The features related to donors are normalized to reflect an donor's interest relative to the rest of the donors. The project features are one-hot encoded. A major feature that proved to be very useful is geographic location of the donor and the schools. A main component of the reommendation algorithm is Geo Search, where possible recommendations are filtered and sorted by distance or around certain geo-locations.

[Part 2](https://github.com/kikimeow/DonorsChoose-Recommender-System/blob/master/DonorsChoose-%20Part%202.%20Exploratory%20Analysis.ipynb) of the notebooks focuses on exploring the dataset to understand the behavior of the donors, where the donations are coming from, and finally, to gain insights into building an effective recommender system, 

[Part 3](https://nbviewer.jupyter.org/github/kikimeow/DonorsChoose-Recommender-System/blob/master/DonorsChoose-%20Part%203.%20Ranking%20Algorithm%20Reasoning%20%26%20Methods.ipynb) of the notebooks explains the intuition behind the e-mail recommendation system, why the donor's behaviors support this approach, and the performance of the recommender algorithm.

Below are the version of the Python packages utilized:
* numpy 1.14.0
* pandas 0.22.0
* requests 2.18.4
* sklearn 0.19.1
* seaborn 0.8.1
* matplotlib 2.1.2
* plotly 2.7.0

To follow the notebooks, please save the six data files to a directory named "data". The notebooks need to be run in sequence. [Google Maps Platform](https://cloud.google.com/maps-platform/) is utilized to obtain geocoding data.  A valid API key would be required to make the API requests.  To view Part 2. Exploratory Analysis properly with the charts produced using Plotly, please see this [link](https://nbviewer.jupyter.org/github/kikimeow/DonorsChoose-Recommender-System/blob/master/DonorsChoose-%20Part%202.%20Exploratory%20Analysis.ipynb). JavaSript-based browser plotting libraries cannot function in pages rendered directly by GitHub.  


