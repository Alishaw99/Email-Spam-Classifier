# email-spam-classifier-new
End to end code for the email spam classifier project
Many email services today provide spam filters that are able to classify emails into spam and non-spam email with high accuracy. SVMs will be used to build a spam filter.

A SVM classifier will be trained to classify whether a given email, x
, is spam (y=1)
 or non-spam (y=0)
. In particular, each email should be converted into a feature vector x∈Rn
.

The dataset is based on a subset of the SpamAssassin Public Corpus and only the body of the email will be used (excluding the email headers).
In processEmail, the following email preprocessing and normalization steps have been implemented:

Lower-casing: The entire email is converted into lower case, so that captialization is ignored (e.g., IndIcaTE is treated the same as Indicate).
Stripping HTML: All HTML tags are removed from the emails. Many emails often come with HTML formatting; we remove all the HTML tags, so that only the content remains.
Normalizing URLs: All URLs are replaced with the text “httpaddr”.
Normalizing Email Addresses: All email addresses are replaced with the text “emailaddr”.
Normalizing Numbers: All numbers are replaced with the text “number”.
Normalizing Dollars: All dollar signs ($) are replaced with the text “dollar”.
Word Stemming: Words are reduced to their stemmed form. For example, “discount”, “discounts”, “discounted” and “discounting” are all replaced with “discount”. Sometimes, the Stemmer actually strips off additional characters from the end, so “include”, “includes”, “included”, and “including” are all replaced with “includ”.
Removal of non-words: Non-words and punctuation have been removed. All white spaces (tabs, newlines, spaces) have all been trimmed to a single space character.
