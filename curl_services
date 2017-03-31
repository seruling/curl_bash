#!/bin/bash

for target in 192.168.1 192.168.10 172.11.19 ##the 1st 3 part of targeted.
do
  echo "------"
  echo "$target"
  for j in 80 443 ##port
  do
    echo "$target.x:$j"
    for i in {1..254}  ##append class-c to the target. 
    do
       echo "$target.$i:$j"
       curl -k --head -m 5 http://$target.$i:$j/;
    done
  done
done
