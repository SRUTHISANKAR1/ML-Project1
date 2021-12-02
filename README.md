# ML-Project1
Hotel Rating Classification(Text Classification)
Business Objective:This is a sample dataset  which consists of 20,000reviews and ratings for different hotels and our goal is to examine how travellers are communicating their positive and negative experiences in online platforms for staying in a specific hotel and major objective is what are the attributes that travellers are considering while selecting a hotel. With this manager can understand which elements of their hotel influence more in forming a positive review or improves hotel brand image.


Basic Understanding of Data:
          1.Dataset contains 20491 observations and 2 variables(Review and Rating)
          2.Review is object type and Rating is integer type
          3.Dataset has no null values
          4.Rating column has 5 unique values. Rating 1 to 5
          5.This dataset is biased or imbalanced
          6.Most of the reviews have  wordlength below 150 and a few have more than 250 words
          
          
Text Preprocessing :In text classification, text preprocessing is the first step in the process of building a model. Whenever we have textual data, we need to apply several pre-processing steps to the data to transform words into numerical features that work with machine learning algorithms.I used NLTK library for text preprocessing.
# Text Preprocessing
            1 - Tokenization
            2 -Normalization
            3 - Removing Numbers
            4 - Removing Punctuations
            5 - Stopwords Removal
            6- Lemmatization
            
            
#Word Cloud: Visualization Technique in which the size of each word will represent the frequency of that text data.
From cleaned review data - the most repeated words are 'room','time','day','great','resort','nice','beach','good','night',
'breakfast','restaurant'.



#Sentiment Analysis Using TextBlob: 
          Sentiment Analysis is the process of determining whether a piece of writing is positive, negative or neutral.
          TextBlob gives two scores Polarity scores and Subjectivity scores.
          Polarity is float which lies in the range of [-1,1] where 1 means positive statement and -1 means a negative statement. subjectivity is a matric between 0 and 1(1 is
          highly subjective)
          94.3%reviews are positive based on the polarity score.So data is highly biased or imbalnced
          
          
          
Top positive features/reviews related to hotel on the basis of N-grams and wordcloud are
              staff helpful, friendly and efficient
              Great Location
              Room clean and nice
              Highly recommend
              Flat screen Tv
              Free Wifi and wonderful server
              free and best breakfast
              wonderful stay
              Free wine,tea and coffee service
              Bathroom attractive ,large with great soaking tub
              Car service price is reasonable
              Huge open space
              good lighting
              large and good building
 
 
 
Top negative points to be noted to improve the hotel's brand image on the basis of Ngrams and wordcloud are
                Worst hotel stayed,Awful night stay,Hotel charges additional charges on credit card,Worst vacation,Horrible experience
                Staff and room service related:
                Staff unwelcoming and rude
                Staff smoking intentionally,cigerette smell in room
                Terrible service
                worst 
                Room and infrastructure related     
                Rooms like hospital rooms
                beds hard,blanket rough
                Small double bed
                nasty frige with odor of rotten vegetables
                Dirty and tiny carpet
                Geyser issue-took cold shower
                Noisy elevator
                Tiles loose
                Broken switches and sagged LCD Tv
                Digital box not working
                AC not working
                Dirty bathroom
                Noise issue:
                Cant sleep in night due to the sounds of  walking and talking
                Noisy neighbours
                Noise from road ,can't sleep,wink night
                
                
                
                
Topic modeling: 
          Topic Modeling is statistical modeling for discovering the abstract that occurs in a collection of documents.
          It helps to uncover the hidden structure in a collection of texts
          Most common algorithms used to perform topic modeling are 
          Latent Dirichlet Allocation(LDA)
          Latent Semantic Analysis (LSA)
          Probabilistic Latent Semantic Analysis(PLSA)
          
          
          
Feature Extraction:          
          Machine only knows numbers .So here we have to convert text data into a numerical format called vectors (Words in reviews are converting into vectors). 
          The process of conversion of unstructured text data into structured format is called Feature Extraction
          
          
Feature extraction techniques:
          Bag  Of Words(Count Vectorization)
          TFIDF  Vectorization
          Word Embedding(Word2Vec)
          
          
#BOW only give zeroes and ones ,doesn't give the idea of importance of words


#TFIDF Vectorization:
          In TFIDF we get different values rather than zeroes and 1's
          TFIDF follows a weighting scheme &it gives an idea about how important a word is.
          
          
          
          
#Word2Vec:
          In which each word is represented by using a vector in three-dimensional space. Words with similar meanings should have similar representations. 
          These representation helps to identify synonyms, antonyms, and various other relationship between words.
          Word2Vec uses a simple neural network.
          in Word2Vec feature extraction a word is known by the neighborhood words.
          Word2Vec helps to predict what word comes next and what is context of the word to be used. Word2Vec predict the target word based on the context word and viceversa
          
          
          
 #Model Building:
          Random Forest Classifier
          Support Vector Machine
          Logistic Regression
          Boosting  #Comparatively better model is XGB model   *#84% accuracy
          KNN
          Decision Tree
          Naive Bayes
          
          
          
I classified reviews based on the rating and labelled the reviews ,
positive (Rating>3) , neutral(Rating=3) and negative(Rating<3)



#Data set is biased so done resampling techniques
We tried to improve the model accuracy by using a resampling technique named SMOTE(Synthetic Minority Oversampling Technique). 
We got good accuracy for Random Forest Classifier(96.4) and Logistic Regression(98.34)




#Deployment done by using
          streamlit
          Flask




