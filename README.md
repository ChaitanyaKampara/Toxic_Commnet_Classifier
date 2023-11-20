

"# CUSTOMER_PERSONALITY_ANALYSIS" 
=======
# Toxic_Commnet_Classifier

# 1.) IMPORTING LIBRARIES
import all necessary libraries like :
pandas <br>
numpy <br>
seaborn <br>
all nlp libraries like : <br>
nltk <br> 
stopwords <br>
wordnetlemmatizer <br>
word_tokenize,sent_tokenize <br>
PorterStemmer,LancasterStemmer,SnowballStemmer 

# 2.) NULL VALUES
Check null values <br>
o/p = There are no values present in dataset

# 3.) CHECK VALUE_COUNTS 
Check value counts for each column which shows the nature of the comment <br>
The o/p will be 0 , 1 for every checked column <br>
0 : NO<br>
1 : YES<br>

# 4.) DATA VISUALIZATION
Before visualizing 1st extract new dataset(sentencetype_graph) from the given dataset(df) <br>
sentencetype_graph = df.iloc[:,2:].sum() [indicates all rows from 3rd column]

# 5.) CLEAN DATA
There are so many unwanted charecters , symbols etc in df[comment_text] for cleaning this we are => <br>
importing re : <br>
Removing: alphanumeric , punchuation_lower , remove(/n) , remove_non_ascii <br>

# 6.) CREATE SEPARATE DATAFRAMES FOR EACH COLUMN
For insult column create a df called Insulting_comment_df it contains only 3 columns : ['id','comment_text','insult'] <br>
code : Insulting_comment_df=df.loc[:,['id','comment_text','insult']] <br>
similarly create for every column

# 7.) WORDCLOUD
Used to visualize data which words are repeting more those will be printed largely

# 8.) BALENCING COLUMNS
we are fixing or restriicting only 5000 rows for each column <br>
we are creating 2 columns as o/p for every 1 column one is labelled as YES and other is labelled as NO <br>
total we are creating 10 columns at the end we are combining every NO and YES of same column to combined_column

# 9.) MODEL IMPLEMENTATION
Import new libraries responsible for model implementations : <br>
LOGISTIC REGRESSION <br>
SVC [ LINEAR ] <br>
NAIVE_BAYES [MULTINOMIALNB , BERNOULLINB] <br>
RANDOM_FOREST <br>
KNN<br>

# 10.) MODEL_EVALUTION
METRICS resposible for deciding performance : <br>
f1_score <br>
precision_score <br>
recall_score <br>
precision_recall_curve <br>
fbeta_score <br>
confusion_matrix <br>
roc_auc_score <br>
roc_curve <br>
 <br>
calculate f1score for every model and check which models accuracy is best

# 11.) CHECKING COMMENT TOXICNESS
FITTING TRAIN DATA TO VECTORIZER(tfidf) and  TO MODEL RANDOMFOREST
GIVE A COMMENT AND CHECK THE ACCURACY OF THE COMMENT BEING TOXICNESS
>>>>>>> f3568fc331d5717a48723d2e11fdffd8d3d9b2a3
