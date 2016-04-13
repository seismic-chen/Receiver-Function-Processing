# Receiver-Function-Processing
This repo contains receiver function (RF) routines for my RF project
Receiver Function HK Analysis

This notes provide a detailed description of receiver HK analysis for the purpose of 1) help me think through the problems, 2) do some bookkeeping the previous works and 3) benefit any potential guy who may work on this project in the future.

All the work are saved in new_rfun/HK/HK_yunfeng directory

1.	Data preparation
Update the events list.  ehdf format is no longer available after August 2013.  QuakeML is the most popular event catalog (need time to learn it).  Currently, I am using the csv file provided by USGS: http://earthquake.usgs.gov/earthquakes/search/, where you can download the events catalog based on your points of interest.  After download the csv file, save it into 
/home/yunfeng/20_30/research/earthquake_catalog
directory.  Then run matlab code generate_events_file.m to generate the monthly event file.
Seismic data are from 5 networks:  CRANE, RAVEN, CNSN, USArray and CANOE.
CRANE: /media/disk2/lu/tomo_data_final
RAVEN:  /home/yunfeng/Data_request/RV_data
CANOE: /home/yunfeng/Data_request/XN_data
USArray: /home/yunfeng/Data_request/tomo_data
CNSN:  There are still problems with downloading data from CNSN, as their data requesting system, autoDRM, fail to respond when submitting data request through email.  For this reason, I only used CNSN data before June, 2011.

Apr. 11, 2016, I am trying to request the data again.   The AutoDRM file are stored in /home/yunfeng/Data_request/CNSN_data/autodrm/storage.  mailCNSN.csh  Send them out directly using Gmail works, however, the number of events requested each time can not exceed a certain number.  Too many requests (e.g., 100 at a time) in one email will likely to piss off their system and you will never get a word from them... 10 seem to be a good number.

2.  Preprocessing
Raw seismic data are generally lack of necessary header information.  Hence, we need to associate the raw data with 


