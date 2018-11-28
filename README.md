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
