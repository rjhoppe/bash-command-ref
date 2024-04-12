#!/bin/bash

# Use quotes when you want to include a space in an entry
friends=(Kyle Marc Jem "Brian Holt" Sarah)

echo My second friend is ${friends[1]}

for friend in ${friends[*]}
do
    echo friend: $friend
done

# The ${#friends[*]} is how you tell bash to calc length
echo "I have ${#friends[*]} friends"
