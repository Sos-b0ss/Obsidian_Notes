What is an Email Header?:

"Header" is basically a section of the mail that contains information such as sender, recipient and date. In addition, there are fields such as "Return-Path", "Reply-To", and "Received". Below you can see the header details of a sample email.
\
![[Pasted image 20220710131554.png]]
\
What does the Email Header do?:
- **Enables Shipper and Recipient Identification**

Thanks to the "From" and "To" fields in the header, it is determined from whom an email will go to whom. If we look at the email above that you downloaded in "eml" format, we see that it was sent from the address "ogunal@letsdefend.io"to "info@letsdefend.io"
![[Pasted image 20220710131656.png]]

- **Spam Blocker**  

It is possible to detect spam emails using Header analysis and other various methods. This protects people from receiving SPAM emails.

- **Allows Tracking an Email’s Route**  

It is important to check the route it follows to see if an email came from the right address. If we look at the sample email above, we see that it came from the "ogunal@letsdefend.io" address, but did it actually come from the "letsdefend.io" domain or from a different fake server that mimics the same name? We can use the header information to answer this question.

### Important Fields
**From**  
The "From" field in the internet header indicates the name and email address of the sender.
\
**To**  
This field in the mail header contains the email's receiver's details.
\
It includes their name and their email address. Fields like CC (carbon copy) and BCC (blind carbon copy) also fall under this category as they all include details of your recipients.  
If you want to find out more about carbon copy and blind carbon copy, check out how to use CC and BCC. 
\
**Date**
This is the timestamp that shows when the email was sent.  
In Gmail, it usually follows the format of "day dd month yyyy hh:mmss  
So if an email had been sent on the 16th of November, 2021, at 4:57:23 PM, it would show as Wed, 16 Nov 2021 16:57:23.
\
**Subject**  
The subject mentions the topic of the email. It summarizes the content of the entire message body.
\
**Return-Path**  
This mail header field is also known as Reply-To. If you reply to an email, it will go to the address mentioned in the Return-Path field.
\
**Domain Key and DKIM Signatures**  
The Domain Key and Domain Key Identified Mail (DKIM) are email signatures that help email service providers identify and authenticate your emails, similar to SPF signatures.
\
**Message-ID**  
The Message ID header field is a unique combination of letters and numbers that identifies each mail. No two emails will have the same Message ID.
\
**MIME-Version**  
Multipurpose Internet Mail Extensions (MIME) is an internet standard of encoding. It converts non-text content like images, videos, and other attachments into text so they can be attached to an email and sent through SMTP (Simple Mail Transfer Protocol).
\
**Received**  
The received field lists each mail server that went through an email before arriving in the recipient's inbox. It's listed in reverse chronological order — where the mail server on the top is the last server the email message went through, and the bottom is where the email originated.
\
**X-Spam Status**  
The X-Spam Status shows you the spam score of an email message.  
First, it'll highlight if a message is classified as spam.  
Then, the spam score of the email is shown, as well as the threshold for the spam for the email.  
\
An email can meet either the spam threshold of an inbox or exceed it. If it's too spammy and exceeds the threshold, it will automatically be classified as spam and sent to the spam folder.
\
### How to Access Your Email Header?
**Gmail**:

**1- Open the relevant e-mail**  
**2- Click on the 3 points at the top right "..."**  
**3- Click on the "Download message" button.**
![[Pasted image 20220710131935.png]]
**4- Once Downloaded, open the file with the extension "eml" using any notebook application.

**Outlook:**

**1- Open the relevant e-mail**  
**2- File - > Info -> Properties - > Internet headers**
![[Pasted image 20220710132200.png]]
![[Pasted image 20220710132204.png]]
