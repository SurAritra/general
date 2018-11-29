# general
general_store

useful docker commands
docker image prune -a
docker system prune -a

create os : *.nix

#Find a file with string: 
ls | grep -R -l "500"

#Print all matching lines (without the filename
# or the file path) in all files under the current
# directory that start with "access.log" that
# contain the string "500". Note that there are no
# files named "access.log" in the current directory,
# you will need to search recursively.
find ./* -name "access.log*" |xargs -I {} grep -h 500 {}

#Command to get ipaddress from the all the file search 
find ./* -name "access.log*" |xargs grep -o '[0-9]\{1,3\}\.[0-9]\{1,3\}\.[0-9]\{1,3\}\.[0-9]\{1,3\}'

#Gives the count of all files in the directory
find -L -type f|wc -l

#Sorting a file
cat access.log | sort

#Count of lines in a file that contain GET
ls access.log | xargs grep -c "GET"

#Print sequence
seq 10

#Print ; seperated values in new line
tr \; \\n<s*

#Remove a file with an extension doc
find . -name "*.doc" -exec rm -rf {} \;

#Remove a phrase in all files and subdirectories "challenges are difficult"
sed -i ch **/*xt 

#File extraction,suppose file name is test
#Here passing the elemnets of the file t*==t***.*** =test.txt
#Hence the element is outputed as sum of the file numbers
#File : echo -e "1\n2\n3\n4\n5\n6\n7\n8\n9" > test.txt
jq -s add<t*


