# Toxic_Commnet_Classifier

# 1.) IMPORTING LIBRARIES
import all necessary libraries like pandas , numpy seaborn and all nlp libraries like nltk , stopwords,wordnetlemmatizer,
word_tokenize,sent_tokenize,PorterStemmer,LancasterStemmer,SnowballStemmer
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
