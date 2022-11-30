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
  - Gathering all of the unique words used in all emails and:
    - Checking the amount of times each specific word appeared in the email
    - Checking if each specific word appeared in the email

Ones we have this information for each email we run a Logistic Regression model in order to best seperate the spam emails using these features. 
- We use Logistic Regression since most of the features are linearly seperatable. 
- Also a Logistic Regression model is simple to explain/visualize.  
- We could also have used a desision tree due to these same reasons.


A UC Berkeley Project Data 100
