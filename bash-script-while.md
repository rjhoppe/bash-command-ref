#!/bin/bash

# let "NUM_TO_GUESS = ${RANDOM} % 10 + 1"
NUM_TO_GUESS=$(( $RANDOM % 10 + 1 ))
GUESSED_NUM=0

echo "guess a number between 1 and 10"

while [ $NUM_TO_GUESS -ne $GUESSED_NUM ]
do
  read -p "your guess: " GUESSED_NUM
done

echo "you got it!"
