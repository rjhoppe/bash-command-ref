#! /bin/bash

# Takes in argument and reads user input
DESTINATION=$1
read -p "enter a file prefix: " FILE_PREFIX

# z flag = empty string
if [ -z $DESTINATION ]; then
  echo "no path provided, defaulting to ~/temp"
  DESTINATION=~/temp
fi

mkdir -p $DESTINATION
cd $DESTINATION
# Creates files 1-10 with user input for FILE_PREFIX preceding the file number
touch ${FILE_PREFIX}{1..10}.txt
echo done
