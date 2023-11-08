#!/bin/bash

grep "$1" /etc/hosts > /dev/null
grep "$2" /etc/hosts > /dev/null

if [ $? != 0 ];
then echo "$1" "$2" >> /etc/hosts
else echo "Este dominio y esta IP ya existen" 
fi
