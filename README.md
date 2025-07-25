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

### 🛠 Prerequisites
Make sure you have the following installed:
- **VSCode**
- **Node.js**
- **npm**

 ### ⬇️ Installing
  Install Node.js and npm 
   - Ensure Node.js is installed on your local system via [Node.js official website](https://nodejs.org/en).  
   - Install the required npm dependencies by running the following command in the terminal:
     
   ```bash
     npm install
   ```
### Running the Application

Clone the Repository:

```bash
git clone https://github.com/trjoshi3011/Delta-x-UN.git
cd sp25UN
```

Install Dependencies

```bash
npm install
```

Run the Development Server:

```bash
npm start
```

The app will be running at: 
```bash
http://localhost:3000
```

## 📚 Tech Stack

- **Reacts**: A front-end development framework that allows for reusable components.
- **JavaScript**: A programming language that allows us to create interactivity through state management and event handling.
- **CSS**: A language we used to style the website, allowing it to look modern and fit the UN colors.

## 🛠️ The Process

### Front-End Process
**Today at the UN Feature**  
We used JavaScript to create a horizontal scroll that allows the page to store multiple news stories in a small area:
- The news is represented by a relevant image.
- The news article title appears.
- A scroll bar is present right below to scroll to more stories.
  
**UN Archive Feature**  
We used JavaScript to create a timeline of the relevant events of the UN history:
- The date and event are present in **bold**.
- Each item in the timeline has an external link for more information if a user is interested in learning more.
- The icons and links change state if you hover over them, creating interactivity.

**Read Watch Listen Engage Feature**  
We used JavaScript to create tabs, so the user can click through Read, Watch, Listen, and Engage:
- Only information from the tab the user is on appears.
- Each tab consists of relevant external links that allow the user to go to more sites for more information.
- The tabs and links change state if you hover over them, creating interactivity.

**External Links Feature**  
We used JavaScript to create buttons on the following topics: Main Bodies, Departments/Offices, Resources/Services, Key Documents, News and Media, and Issues/Campaigns:
- When the user hovers over the button, a pop-up appears that shows the user multiple relevant links.
- Each pop-up is scrollable, so the user can see all the links while still preserving space.

**UN Photo Feature**  
We used JavaScript to create buttons that lead users to external sites if they choose to view photos:
- When the user hovers over the button, it changes color, creating interactivity.
- Also, a photo appears on the main page, which we are working to make interactive, so the photo changes on its own at a certain time interval.

**Broadcast Feed and Calendars Feature**  
We used JavaScript to create components so that each group of information is separated and clear:
- Each component has links to external sites so the user can view more information if they choose to.

## 🚧 Challenges

The two biggest challenges we faced were the lack of engagement data on YouTube and not getting access to Instagram comments. For YouTube, we were dealing with around 400 comments, and over 20% of them came from a single video. With such sparse data, it's hard to make strong conclusions about what's working and what isn't. Many of the visualizations we created were useless because there simply wasn't enough data to discern clear trends. The visualizations we used and which showed some trends, were also not ideal for making definitive strategies. 

## 📈 Next Steps

Our next steps involve creating a sentiment classification model trained specifically on the engagement data from Adobe content. First, we plan to manually label each comment from both Photoshop and Firefly content. Then, we plan to use scikit-learn to create baseline classification models like logistic regression and support vector machines. After that, we will fine-tune a large Hugging Face transformer model with our labeled data and evaluate it. Once we create the classification model, we will deploy it with a nice interface using Streamlit.



                  
