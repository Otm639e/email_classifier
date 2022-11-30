# Email Classifier

Ever wonder how your app decides what emails to put into your spam folder?
What makes a spam email different from a regular email:
- Spam emails are emails usually sent in bulk to a large number of recipients from people you don't know, people who are trying to steal some type of information, or people who are offering products. All of which you are not interested in. 
- Problem is, how can we avaoid these types of emails?

Email Classifiers help with this problem! 
In order to distinguish between spam and non-spam emails we will check:
  - Whether the email is a reply (if it is a reply then most likely you will want to see it)
  - Whether the email contains HTML Tags (emails usually don't contain html tags)
  - The number of HTML Tags in an email
  - The number of exclamation marks (Since usually ads put more exclamation marks than people) in an email
  - The length of the email (word count)
  - The number of digits (numbers/integers) in an email
  What best helped:
  - Gathering all of the unique words used in all emails:
    - Randomly selected 6000 of those words (to reduce the model's training time)
    - Checking the amount of times each specific word appeared in the email
    - Checking if each specific word appeared in the email

Ones we have this information for each email we run a Logistic Regression model in order to best seperate the spam emails using these features. 
- We use Logistic Regression since most of the features are linearly seperatable. 
- Also a Logistic Regression model is simple to explain/visualize.  
- We could also have used a desision tree due to these same reasons.

Results:
- Out of all the emails flagged as spam, how many are actually spam (precision):  97.42%
- Out of all the spam emails, how many were actually flagged as spam (recall):  96.19%
- Out of all the non-spam emails, how many were incorrectly flagged as spam (false alarm rate):  0.88%
- Out of all emails, how many were correctly classified (accuracy):  98.37%

Next Steps:
- Using this Logistic Regression model what we could do next is create a website where we can input an email (string) and get back whether that email is spam (boolean). This website would also show the intermediate steps according the model's equation (weights on each feature).
- This would be great for people learning what happens underneath the hood of similar machine learning classifiers.

A UC Berkeley Project Data 100
