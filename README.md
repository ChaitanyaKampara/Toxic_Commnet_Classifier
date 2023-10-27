# Toxic_Commnet_Classifier

# 1.) IMPORTING LIBRARIES
import all necessary libraries like 
pandas 
numpy
seaborn 
all nlp libraries like
nltk 
stopwords
wordnetlemmatizer
word_tokenize,sent_tokenize
PorterStemmer,LancasterStemmer,SnowballStemmer

# 2.) NULL VALUES
Check null values o/p = There are no values present in dataset

# 3.) CHECK VALUE_COUNTS 
Check value counts for each column which shows the nature of the comment
The o/p will be 0 , 1 for every checked column 
0 : NO
1 : YES

# 4.) DATA VISUALIZATION
Before visualizing 1st extract new dataset(sentencetype_graph) from the given dataset(df)
sentencetype_graph = df.iloc[:,2:].sum() [indicates all rows from 3rd column]

# 5.) CLEAN DATA
There are so many unwanted charecters , symbols etc in df[comment_text] for cleaning this we are
importing re :
Removing: alphanumeric , punchuation_lower , remove(/n) , remove_non_ascii 

# 6.) CREATE SEPARATE DATAFRAMES FOR EACH COLUMN
For insult create a df called Insulting_comment_df it contains only 3 columns : ['id','comment_text','insult']
code : Insulting_comment_df=df.loc[:,['id','comment_text','insult']]
similarly create for every column

# 7.) WORDCLOUD
Used to visualize data which words are repeting more those will be printed largely

# 8.) BALENCING COLUMNS
we are fixing or restriicting only 5000 rows for each column 
we are creating 2 columns as o/p for every 1 column one is labelled as YES and other is labelled as NO
total we are creating 10 columns at the end we are combining every NO and YES of same column to combined_column

# 9.) MODEL IMPLEMENTATION
Import new libraries responsible for model implementations :
LOGISTIC REGRESSION
SVC[LINEAR]
NAIVE_BAYES [MULTINOMIALNB , BERNOULLINB]
RANDOM_FOREST
KNN

# 10.) MODEL_EVALUTION
METRICS resposible for deciding performance :
f1_score
precision_score
recall_score
precision_recall_curve
fbeta_score 
confusion_matrix
roc_auc_score
roc_curve

calculate f1score for every model and check which models accuracy is best

# 11.) CHECKING COMMENT TOXICNESS
FITTING TRAIN DATA TO VECTORIZER(tfidf) and  TO MODEL RANDOMFOREST
GIVE A COMMENT AND CHECK THE ACCURACY OF THE COMMENT BEING TOXICNESS
