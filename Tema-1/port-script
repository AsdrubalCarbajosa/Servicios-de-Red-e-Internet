#!/bin/sh

grep $1 "/etc/apache2/ports.conf" >> /dev/null
if [ $? -ne 0 ];
then echo "Listen $1" >> "/etc/apache2/ports.conf"
else echo "Este puerto ya existe en ports.conf"
fi
