# I Hacked-LA-2023
- "submit" your work by creating a pull request as detailed in the README.md.

List your group members:
> Christi Denny, Yuchen Zhang, Chloe Li

# This Project<br>
> Link to presentation: 
> Give a brief description of the final product:
>  There are some findings we have obtained.
>  1. On average, if students spend more time on Canvas, they are likelier to get a higher score. But it is not a guaranty for a ggod grade, inefficiency is also an essential element.
>  2. Users are most active in the latter part of the day, from Sundays to Thursdays, but on Fridays, te activity is the lowest in a week. The suggestion for the professor would be to release materials on days that students are active.
>  3. A word cloud representing data discussion forums illustrates the frequency of specific terms. Topics including discussion, assignment and elearning are on the top.

# Reflection
## Approach
> What was your approach to the dataset? What problem did you want to solve? What technology did you decide to use? How did your team split the work?
> We did data analysis, data visualization and text mining on the datasets.
> We would like to see if there was any relationship between student's activities on canvas and their academic performance, how to iimprove one's study performance, what kind of modules or activities they were most intereted in.
> We use python and Tableau to analyze data.
>  We work on different datasets individually. If one member had some findings, we discussed it together.
 
## Wins / Challenges<br>
> Describe some wins / challenges. What did you learn? What would you do differently next time?
> Wins: What we have found is more or less what we expected.
> Challenges: The datasets are small and not perfect, so it is challenging to clean the data, find connections between datasets, and find insights at the beginning.


# Code
> import seaborn as sns
> import matplotlib.pyplot as plt
> import pandas as pd
> import matplotlib.pyplot as plt
> df_events = pd.read_csv('./data/events.csv')
> df_events.head()
>df_assignment = pd.read_csv('./data/assignments.csv')
>df_discussion_topics= pd.read_csv('./data/discussion_topics.csv')
>df_discussion= pd.read_csv('./data/discussions.csv')
>df_enroll= pd.read_csv('./data/enrollments.csv')
>df_file= pd.read_csv('./data/files.csv')
>df_grade= pd.read_csv('./data/gradebook.csv')
>df_module= pd.read_csv('./data/module_items.csv')
>df_page= pd.read_csv('./data/pages.csv')
>discussion_topic = df_discussion.value_counts('discussion_topic_title')
>df_discussion.sort_values('timestamp',asce)
>df_discussion.groupby('discussion_topic_title')['post_message_length'].mean().sort_values(ascending=False)
>df_discussion['timestamp'] = pd.to_datetime(df_discussion['timestamp'],format='mixed')
>df_enroll.sort_values('total_activity_time', ascending = False)
>def grade(x):
>    if x >= 90:
>        Grade = 'A+'
>    elif x >= 85:
>        Grade = 'A'
>    elif x >= 80:
>        Grade = 'A-'
>    elif x >= 76:
>        Grade = 'B+'
>    elif x >= 72:
>        Grade = 'B'
>    elif x >= 68:
>        Grade = 'B-'
>    elif x >= 62:
>        Grade = 'C'
>    elif x >= 60:
>        Grade = 'D'    
>    else:
>        Grade = 'F'     
>    return(Grade)       
>import numpy as np
>df_grade = df_grade[2:]
>df_grade.dtypes
>df_grade['Assignment 1 Current Score'] = pd.to_numeric(df_grade['Assignment 1 Current Score'], errors='coerce')
>df_grade['Assignment 2 Current Score'] = pd.to_numeric(df_grade['Assignment 2 Current Score'], errors='coerce')
>df_grade['Assignment 3 Current Score'] = pd.to_numeric(df_grade['Assignment 3 Current Score'], errors='coerce')
>df_grade['Current Score'] = pd.to_numeric(df_grade['Current Score'], errors='coerce')
>df_grade['Participation & engagement Current Score'] = pd.to_numeric(df_grade['Participation & engagement Current Score'], errors='coerce')
>df_grade.describe()
>df_discussion[df_discussion['actor_id'] == 'INSTRUCTOR'].sort_values('timestamp',ascending= False)
>
>df_discussion.sort_index().drop_duplicates('discussion_topic_title',keep='first')
>df_grade.sort_values('Current Score',ascending = False)
>
>df_grade.sort_values('Assignment 1 Current Score',ascending = False)
>
>df_grade_enroll = df_grade.merge(df_enroll,left_on='Student',right_on='user_id',how='left')
>df_grade_enroll.dtypes
>
>df_grade_enroll['Grade']=df_grade_enroll['Current Score'].apply(grade)
>df_grade_enroll[df_grade_enroll['Grade'] == 'F']
>
>avg_time = df_grade_enroll.groupby('Grade')['total_activity_time'].mean()
>
>data = {
>   'Grade': ['A+', 'A', 'A-', 'B+', 'B', 'B-', 'C', 'F'],
>    'total_activity_time': [426200.0, 667417.8, 538334.0, 645786.4, 492165.0, 175719.0, 1015778.0, 0.0]
>}
>
>series = pd.Series(data['total_activity_time'], index=data['Grade'])
>
># Create a bar plot
>plt.figure(figsize=(8, 6))
>series.plot(kind='bar', color='skyblue')
>plt.xlabel('Grade')
>plt.ylabel('Total Activity Time')
>plt.title('Total Activity Time by Grade')
>plt.savefig('Grade vs Time')
>plt.show()
>df_events['event_time'] = pd.to_datetime(df_events['event_time'],format='mixed')
>df_events['event_time'][1]
>## Group the events by day and count the number of events per day
>daily_events = df_events['event_time'].dt.date.value_counts().sort_index()

>## Create a line graph
>plt.figure(figsize=(10, 6))
>plt.plot(daily_events.index, daily_events.values, marker='o', linestyle='-')
>plt.title('Events per Day')
>plt.xlabel('Date')
>plt.ylabel('Number of Events')
>plt.xticks(rotation=45)
>plt.grid(True)

>## Display the graph
>plt.tight_layout()
>plt.show()

>import datetime

># Group the events by day and count the number of events per day
>daily_discussion = df_discussion['timestamp'].dt.date.value_counts().sort_index()

># Create a line graph
>plt.figure(figsize=(10, 6))
>plt.plot(daily_discussion.index, daily_discussion.values, marker='o', linestyle='-')
>plt.title('Discussions per Day')
>plt.xlabel('Date')
>plt.ylabel('Number of Discussion')
>plt.xticks(rotation=45)
>plt.grid(True)

>vertical_line_date = datetime.date(2033, 2, 9)
>plt.axvline(x=vertical_line_date, color='red', linestyle='--', label='Vertical Line')

>vertical_line_date = datetime.date(2033, 3, 9)
>plt.axvline(x=vertical_line_date, color='red', linestyle='--', label='Vertical Line')

>vertical_line_date = datetime.date(2033, 4, 9)
>plt.axvline(x=vertical_line_date, color='red', linestyle='--', label='Vertical Line')


># Display the graph
>plt.tight_layout()

>plt.savefig('discussions per day')
>plt.show()

>df_grade[['Assignment 1 Current Score','Assignment 2 Current Score','Assignment 3 Current Score','Participation & engagement Current Score','Current Score']].corr()

># Basic descriptive statistics
>print(df_discussion[['discussion_topic_message_length', 'post_message_length']].describe())

>df_discussion

># Count of posts by actor
>posts_by_actor = df_discussion['actor_id'].value_counts()
>print(posts_by_actor.head())

># Sum of likes by actor
>likes_by_actor = df_discussion.groupby('actor_id')['count_of_likes'].sum()
>print(likes_by_actor.sort_values(ascending=False).head())

># Convert 'timestamp' to datetime
>df_discussion['timestamp'] = pd.to_datetime(df_discussion['timestamp'])

># Set 'timestamp' as index
>df_discussion.set_index('timestamp', inplace=True)

>monthly_posts = df_discussion['post_id'].resample('M').count()
>print(monthly_posts)
>topic_counts = df_discussion.groupby(['discussion_topic_id', 'discussion_topic_title']).size()
>## Sort the counts in descending order to find the most discussed topics
>popular_topics_with_titles = topic_counts.sort_values(ascending=False)

>## Display the top 5 most discussed topics with titles
>print(popular_topics_with_titles.head())

>## Average post message length by membership role
>avg_length_by_role = df_discussion.groupby('membership_role')['post_message_length'].mean()
>print(avg_length_by_role)

>import seaborn as sns
>import matplotlib.pyplot as plt

>## new column for the hour of the day and the day of the week
>df_discussion['hour'] = df_discussion.index.hour
>df_discussion['day_of_week'] = df_discussion.index.day_name()

>## for the heatmap; count the number of posts in each hour for each day
>activity_matrix = df_discussion.groupby(['day_of_week', 'hour']).size().unstack(fill_value=0)

>## Order the days of the week starting from Monday
>ordered_days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
>activity_matrix = activity_matrix.reindex(ordered_days)

>## Plot the heatmap
>plt.figure(figsize=(12, 7))  # You can adjust the size as needed
>sns.heatmap(activity_matrix, cmap='viridis', linewidths=.5, annot=True)

>## Add labels and a title
>plt.title('Activity Heatmap (Posts per Day and Hour)')
>plt.xlabel('Hour of the Day')
>plt.ylabel('Day of the Week')

>plt.savefig('heatmap')

>## Show the plot
>plt.show()

>from nltk.corpus import stopwords
>from nltk.tokenize import word_tokenize
>from wordcloud import WordCloud
>import matplotlib.pyplot as plt
>import nltk
>from nltk import FreqDist

>nltk.download('stopwords')
>nltk.download('punkt')

>## Assuming 'discussion_subentry_count' is a column in your dataframe
>## We sort the dataframe based on 'discussion_subentry_count' in descending order
>df_discussion_topics_sorted = df_discussion_topics.sort_values(by='discussion_subentry_count', ascending=False)

>## Select the top N discussions
>top_discussions = df_discussion_topics_sorted.head(10)

>stop_words= stopwords.words('english')

>## Get the titles of the top discussions
>top_titles = ' '.join(top_discussions['title'].dropna().values)

>## Tokenize and clean the titles as before
>top_tokens = word_tokenize(top_titles)
>top_words = [word.lower() for word in top_tokens if word.isalpha() and word.lower() not in stop_words]

>## Frequency distribution for top words
>top_fdist = FreqDist(top_words)
>for word, frequency in top_fdist.most_common(10):
>    print(f'{word}: {frequency}')

>## Generate a word cloud image for top discussions
>top_wordcloud = WordCloud(width=800, height=400, background_color='white').generate(' '.join(top_words))

>## Display the word cloud
>plt.figure(figsize=(15, 8))
>plt.imshow(top_wordcloud, interpolation='bilinear')
>plt.axis('off')
>plt.savefig('wordcloud')
>plt.show()
