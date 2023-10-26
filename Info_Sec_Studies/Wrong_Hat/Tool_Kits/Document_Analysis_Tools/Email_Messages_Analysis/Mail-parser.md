Sources:
https://github.com/SpamScope/mail-parser
\
mail-parser is not only a wrapper for [email](https://docs.python.org/2/library/email.message.html) Python Standard Library. It give you an easy way to pass from raw mail to Python object that you can use in your code. It's the key module of [SpamScope](https://github.com/SpamScope/spamscope).
\
mail-parser can parse Outlook email format (.msg). To use this feature, you need to install `libemail-outlook-message-perl` package.
\
For Debian based systems:
```
$ apt-get install libemail-outlook-message-perl
```
\
For more details:
```
$ apt-cache show libemail-outlook-message-perl
```
