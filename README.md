# BigData example based on Airline on time data

# Basic Flow

Get data->preprocess->import to bigdata platform->further process

# Get Airline data

#!/bin/bash

baseurl=http://stat-computing.org/dataexpo/2009

myPath=airline-data

if [ ! -d "$myPath" ];
then
    mkdir "$myPath"
fi


for year in `seq 1987 2008`;
do
    echo "Getting " $year "'s data";
    datafile=$year.csv.bz2
    wget $baseurl/$datafile
    mv $datafile $myPath
done

echo "Done"
