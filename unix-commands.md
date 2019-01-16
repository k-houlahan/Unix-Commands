###Unix Codes###

To redirect standard output to a file, the ">" character is used. If you want the new results to be appended to an existed file instead, use ">>"

&& = AND           #ex.: mkdir fold1 && cp file fold1/.
|| = OR            #ex.: cp file fold1/. || cp file fold2/.

General shell synthax:
command -option target

For help:
command --help

General Navigation: 
cp* /home/tom/backup #copy all files from one directory to another 
scp/                 #secure copy
rm file name         #remove files 
mv oldname newname(or place) #move or rename files 
nohup #runs programs in the background * Note you need to create a log file for this * 
        #ex: nohup asreml fat.asr > fat.out  (fat.out is the output file for the log) 
chgrp daiclu <filename> # allows read access to the group
chmod g+w <filename>   #allows writing permission for the members of the group for that file 
chmod g+w* # allows modification to all files 
chgrp -R daiclu <dirname> #recursively allows group reading permission 



tr''','<filename>newfilename # this changes what is in the first '' to what is in the second '' 

#### AWK ####

awk 'NF <13 {print} filename  #print the rows that have less than 13 columns 
awk '{sub(/\./," ",$1)};1' filename  #substitute the "." with a space in column 1


#### SED  ####
sed -e 's/\s\+/,/g' orig.txt > modified.txt #this will change blank spage of any size into a single comma 
sed -i.bak 1i"name1,name2,name3" file.ext # this will add in a header to a CSV file while saving the old file in a backup
