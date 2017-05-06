Detection-of-Trending-Topic-Communities -> Datasets-Code
Bridging Twitter Content Creators and Distributors: datasets used, main code in Python, and results file

The analysis were performed on a dataset specifically built to collect information about trending topics on Twitter, which was presented in "Real-Time Classification of Twitter Trends", by Zubiaga, A., Spina, D., Fresno, V. and Martínez, R. It is available online in http://nlp.uned.es/~damiano/datasets/TT-classification.html. The dataset contains 1,036 trending topics, which are associated to 567,452 tweets from 348,757 different users. However, in order to form the graph and detect the trending topic communities, according to our method proposed, the information about the tweets and the users who posted them is not enough. Indeed, we need to have the "following relationship" between the content creators, and the "following relationship" between the content distributors. This was collected by querying the Twitter API, for the first 368 topics (due to the limitations imposed by the API on the number of calls that could be made).

Detection-of-Trending-Topic-Communities_Datasets-Code contains json, gexf and ipynb files obtained as a result of the research project . The data corresponds to 
information generated during strikes agaist the government of Ecuador (2015 and 2016). In detail, the files are:

- creators.json 
The creators of tweets per trending topic, the data here is provided for all 1036 trending topics.

- distributors.json 
The distributors who made retweets per trending topic, the data here is provided for all 1036 trending topics.

- unique_users_Creators_Distrib_perTopic368.json
The unique ids of the creators and distributors per trending topic. The data correspond to the 368 trending topics in our project.

- trending_topics_list368.json
The list of the 368 trending topics in our project.

- FollowersCreators_perTrendingTopic (too big, ask to lorena.recalde@upf.edu)
Folder with a list of files with the followers of the creators. A file corresponds to a trending topic creators (and their followers). Those files are used to create the graphs.

- FollowersDistributors_perTrendingTopic (too big, ask to lorena.recalde@upf.edu)
Folder with a list of files with the followers of the distributors. A file corresponds to a trending topic distributors (and their followers). Those files are used to create the graphs.

- Retweeting_graphs368
Folder with the graphs resulting from the application of the RBC method. There are two versions of the graphs per trending topic: json format and gexf format.

- Following_graphs_Creators368
Folder with the graphs resulting after the detection of the "following relationship among creators" per trending topic. There are two versions of the graphs per trending topic: json format and gexf format. Files in the folder FollowersCreators_perTrendingTopic used. These graphs are needed to apply the proposed method TreToc communities.

- Following_graphs_Distributors368
Folder with the graphs resulting after the detection of the "following relationship among distributors" per trending topic. There are two versions of the graphs per trending topic: json format and gexf format. Files in the folder FollowersDistributors_perTrendingTopic used. These graphs are needed to apply the proposed method TreToc communities.

- Our_Method_TretocGraphs368
Folder with the graphs resulting from the application of the TreToc method. The graphs in Retweeting_graphs368, Following_graphs_Creators368, and Following_graphs_Distributors368 were joint. There are two versions of the graphs per trending topic: json format and gexf format.

- Graphs_Extraction.ipynb
Source code implemented to create the graphs for the RBC method and TreToc method.

- Community_Detection_Metrics.ipynb
Source code implemented to calculate the metrics that validate the method proposed. The values for the metrics were calculated over the RBC graphs and TreToc graphs.

- Data_Analysis_Results.numbers
Data that shows the results obtained.

We also provide all the necessary steps to reproduce the experiments on detection of trending topic communities 
in the paper referenced below. For more details on how these files were generated, we refer to the following 
scientific publication. We would highly appreciate if scientific publications of works partly based on the 
Detection-of-Trending-Topic-Communities_Datasets-Code quote the following publication:

Lorena Recalde, David F. Nettleton, Ricardo Baeza-Yates and Ludovico Boratto. 2017. Detection of Trending Topic Communities: Bridging Content Creators and Distributors. In Proceedings of HT ’17, Prague, Czech Republic, July 04-07, 2017, 9 pages.
https://doi.org/http://dx.doi.org/10.1145/3078714.3078735


