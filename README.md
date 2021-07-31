# Spam classification using Spark

Classification of e-mail messages as spam or non-spam using Spark. Process involves loading and preprocessing the email-messages to training and testing classifiers in a distributed way in Spark. Classification of an e-mail is performed using normalised tf-idf vectors as features for Logistic regression, Naive Bayes and SVM classifiers. 

## Background on data

The data consists of four subdirectories [bare, stop, lemm, lemmstop](https://github.com/bragancas/texttest/blob/master/lingspam_public/readme.txt), corresponding to four versions of the corpus. Within each subdirectory email-messages are available as .txt files and are spread out across 10 different parts. Each of the 10 parts consists of a mix of spam and non-spam emails and have 289-291 messages with a total of 2893 messages out of which 289 messages are spam. Each e-mail .txt file consists of the subject followed by the body of the message. The filename of the .txt files indicates whether a message is spam or not, where spam e-mail .txt begins with 'spmsg'.