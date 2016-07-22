# Machine_Learning_on_Spark
Examples with machine learning algorithmes using spark.<br>
Spark runs in four modes:<br>
1. The standalone local mode, where all Spark processes are run within the same Java Virtual Machine (JVM) process<br>
2. The standalone cluster mode, using Spark's own built-in job-scheduling framework<br>
3. Using Mesos, a popular open source cluster-computing framework<br>
4. Using YARN (commonly referred to as NextGen MapReduce), a Hadoop-related cluster-computing and resource-scheduling framework<br>


* [Designing ML Systems](#project1)
* [Data Processing](#project2)
* [Recommendation Engine](#project3)
* [Classification](#project4)
* [Regression](#project5)
* [Clustering](#project6)
* [Dimensionality Reduction](#project7)
* [Advanced Text Processing](#project8)
* [Real-time Streaming](#project9)


<a name="project1">
## Designing ML Systems
</a>
#### Components of a data-driven machine learning system
The high-level components of our machine learning system are outlined in the following diagram. This diagram illustrates the machine learning pipeline from which we obtain data and in which we store data. We then transform it into a form that is usable as input to a machine learning model; train, test, and refine our model; and then, deploy the final model to our production system. The process is then repeated as new data is generated.

#### Data ingestion and storage
Data storage can be complex and involve a wide variety of systems, including HDFS, Amazon S3, and other filesystems; SQL databases such as MySQL or PostgreSQL; distributed NoSQL data stores such as HBase, Cassandra, and DynamoDB; and search engines such as Solr or Elasticsearch to stream data systems such as Kafka, Flume, or Amazon Kinesis.

#### Data cleansing and transformation
• Filtering data: Let’s assume that we want to create a model from a subset of the raw data, such as only the most recent few months of activity data or only events that match certain criteria.
• Dealing with missing, incomplete, or corrupted data: Many real-world datasets are incomplete in some way. This might include data that is missing (for example, due to a missing user input) or data that is incorrect or flawed (for example, due to an error in data ingestion or storage, technical issues or bugs, or software or hardware failure). We might need to filter out bad data or alternatively decide a method to fill in missing data points (such as using the average value from the dataset for missing points, for example).
• Dealing with potential anomalies, errors, and outliers: Erroneous or outlier data might skew the results of model training, so we might wish to filter these cases out or use techniques that are able to deal with outliers.
• Joining together disparate data sources: For example, we might need to match up the event data for each user with different internal data sources, such as user profiles, as well as external data, such as geolocation, weather, and economic data.
• Aggregating data: Certain models might require input data that is aggregated in some way, such as computing the sum of a number of different event types per user.

<a name="project2">
## Data Processing
</a>
#### Obtaining Data
- UCI Machine Learning Repository: This is a collection of almost 300 datasets of various types and sizes for tasks including classification, regression, clustering, and recommender systems. The list is available at http://archive.ics.uci.edu/ml/.
- Amazon AWS public datasets: This is a set of often very large datasets that can be accessed via Amazon S3. These datasets include the Human Genome Project, the Common Crawl web corpus, Wikipedia data, and Google Books Ngrams. Information on these datasets can be found at http://aws.amazon.com/publicdatasets/.
- Kaggle: This is a collection of datasets used in machine learning competitions run by Kaggle. Areas include classification, regression, ranking, recommender systems, and image analysis. These datasets can be found under the Competitions section at http://www.kaggle.com/competitions.
- KDnuggets: This has a detailed list of public datasets, including some of those mentioned earlier. The list is available at http://www.kdnuggets.com/datasets/index.html.

#### Processing and transforming
- Filter out or remove records with bad or missing values: This is sometimes unavoidable; however, this means losing the good part of a bad or
missing record.
- Fill in bad or missing data: We can try to assign a value to bad or missing data based on the rest of the data we have available. Approaches can include assigning a zero value, assigning the global mean or median, interpolating nearby or similar data points (usually, in a time-series dataset), and so on. Deciding on the correct approach is often a tricky task and depends on the data, situation, and one's own experience.
- Apply robust techniques to outliers: The main issue with outliers is that they might be correct values, even though they are extreme. They might also be errors. It is often very difficult to know which case you are dealing with. Outliers can also be removed or filled in, although fortunately, there are statistical techniques (such as robust regression) to handle outliers and extreme values.
- Apply transformations to potential outliers: Another approach for
outliers or extreme values is to apply transformations, such as a logarithmic or Gaussian kernel transformation, to features that have potential outliers, or display large ranges of potential values. These types of transformations have the effect of dampening the impact of large changes in the scale of a variable and turning a nonlinear relationship into one that is linear.


<a name="project3">
## Recommendation Engine
</a>
#### Type of recommendation models
- Content-based filtering: Content-based methods try to use the content or attributes of an item, together with some notion of similarity between two pieces of content, to generate items similar to a given item. These attributes are often textual content (such as titles, names, tags, and other metadata attached to an item), or in the case of media, they could include other features of the item, such as attributes extracted from audio and video content.
- Collaborative filtering: Collaborative filtering is a form of wisdom of the crowd approach where the set of preferences of many users with respect to items is used to generate estimated preferences of users for items with which they have not yet interacted. The idea behind this is the notion of similarity.
- Explicit matrix factorization, Implicit matrix factorization

<a name="project4">
## Classification
</a>

<a name="project5">
## Regression
</a>

<a name="project6">
## Clustering
</a>

<a name="project7">
## Dimensionality Reduction
</a>

<a name="project8">
## Advanced Text Processing
</a>

<a name="project9">
## Real-time Streaming
</a>






