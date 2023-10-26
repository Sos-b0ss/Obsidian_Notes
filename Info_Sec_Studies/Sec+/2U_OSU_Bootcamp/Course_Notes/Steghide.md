[[EOG]] family.jpg 
sudo [[EOG]] family.jpg
echo "This is my hidden message" > hidden_message.txt
ls
sudo steghide embed -cf family.jpg -ef hidden_message.txt 
ls
rm hidden_message.txt 
ls
sudo steghide extract -sf family.jpg 
ls
cat hidden_message.txt 
\
If you want to remove the embedded file after you extract you can use "xf" flag and it will override the embedded image.
