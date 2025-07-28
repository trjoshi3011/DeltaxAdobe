## 🌟 Introduction
This project aims to develop a sentiment analysis model to help Adobe’s Creative Content team assess audience engagement with Adobe Live and Photoshop content across Instagram and Youtube. Using a database with content links, the team will extract comment data from each platform, analyze sentiment, and identify which types of content elicit more positive reactions and engagement. 

## 👥 The Team and Roles

| Name            | Role            | Major                                     |
| --------------- | --------------- | ----------------------------------------- |
| Tanay Joshi   | Project Manager | Data Science & Economics                   |
| Kelley Liang     | Project Manager | Electrical Engineering & Computer Science    |
| Raghav Aggarwal | Senior Analyst  | Computer Science                          |
| Radhika Goyal     | Analyst  | Electrical Engineering & Computer Science                              |
| Nishanth Kairamkonda         | Analyst         | Electrical Engineering & Computer Science                              |

### 🧑‍💻 Running the Application in Google Colab
You don’t need to install anything or clone the repository locally. Just follow these steps:


 ### ✅ Prerequisites
  - A Google account
  - Internet access
  - No local setup required — everything runs in the browser via Google Colab


### ▶️ How to Run
- Click on the Colab link provided
- Once the Colab notebook opens, click:
 ```bash
Runtime → Run all
```
- Wait for the code to execute. You may be prompted to grant Colab permissions the first time.

## 📚 Tech Stack

- **Python**: A versatile programming language used for data processing and analysis.
- **Pandas**: A powerful data manipulation library used for cleaning, transforming, and analyzing structured data.
- **Seaborn**: A statistical data visualization library, used to create informative and attractive charts and graphs.
- **Hugging Face**: An open-source platform providing access to state-of-the-art machine learning models, particularly for natural language processing (NLP).
- **OpenAI API**: A cloud-based API that enables interaction with GPT to generate text and analyze content.

## 🛠️ The Process

**Getting the Data**  
For YouTube, we used the official YouTube API. We passed in a CSV file with links to the YouTube Videos, and the API got us the comments to those videos and other metadata.
- 214 Photoshop comments
- 266 Fireflu comments

For Instagram, we used the  Graph API. The API only allows access to comments by reels posted by Adobe, regardless if it was added as a collaborator.
- 8258 comments in total 

  
**Processing**  
We used Pandas dataframes to store, process, and clean the data. This allowed us to delete rows (i.e, a comment) that we wanted to remove for a visualization. For example, for sentiment visualizations, we wanted to avoid using comments that the Hugging Face model was unsure about. So, through using Pandas, we were easily able to do this.

**Creating Visualizations**  
We used Seaborn to create the visualizations. We would take two variables and plot a fitting graph to represent the relationship between the two variables. Once the graph was plotted, we would see if any insights could be extracted.

**Using Hugging Face**  
We used the "Twitter-roBERTa-base for Sentiment Analysis" model for our initial labeling of the comments for some of the visualizations. 
- Classifies text as Positive, Neutral, or Negative
- Trained on ~58M tweets

**Using GPT**  
We used the OpenAI API to get access to the GPT-4 4o-mini model. We passed in the transcripts of all the YouTube videos that had transcripts, and asked GPT to determine the method of advertisement. 



## 🚧 Challenges

The two biggest challenges we faced were the lack of engagement data on YouTube and not getting access to Instagram comments. For YouTube, we were dealing with around 400 comments, and over 20% of them came from a single video. With such sparse data, it's hard to make strong conclusions about what's working and what isn't. Many of the visualizations we created were useless because there simply wasn't enough data to discern clear trends. The visualizations we used and which showed some trends, were also not ideal for making definitive strategies. 

## 📈 Next Steps

Our next steps involve creating a sentiment classification model trained specifically on the engagement data from Adobe content. First, we plan to manually label each comment from both Photoshop and Firefly content. Then, we plan to use scikit-learn to create baseline classification models like logistic regression and support vector machines. After that, we will fine-tune a large Hugging Face transformer model with our labeled data and evaluate it. Once we create the classification model, we will deploy it with a nice interface using Streamlit.



                  
