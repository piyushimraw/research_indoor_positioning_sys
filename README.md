# Research Documentation on Indoor Positioning System
Please read the following [Wikipedia Indoor Positioning System](https://en.wikipedia.org/wiki/Indoor_positioning_system#Magnetic_positioning)

We have several technology there please pick a technology and do extensive research and provide the following in report so we can evaluate the and come to a conclusion
1. Pros/Cons of Technology
2. Abstract Implementation Idea
3. Reference to some open source libraries
4. Documentations links


## Beacon method for Indoor Positioning System
The most widely library used library is [AltBeacon Library](https://github.com/AltBeacon/android-beacon-library)
[Documentation](https://altbeacon.github.io/android-beacon-library/)

## update 
> @Latest: Nov 21,2017 23:45.



Solution will use client server architecture to fetch the floor plans from server.
Client app will request the floor plan for a building by `HTTP POST` request server will reply with `JSON` contaiing floor plan.
Client app will load the map using that file 
Please Install [Anyplace](https://github.com/piyushimraw/anyplace) and use it to get better understanding of its workings and someone 
- [ ] Test the windows server installation 


## Windows Installation of Anyplace
To install and run windows server follow the following steps.
  1. **Install & Configure Couchbase** Download the latest Couchbase Server Community Edition from [https://www.couchbase.com/downloads](https://www.couchbase.com/downloads). Anyplace v3 has been tested with Couchbase 4.5, but compatibility with later versions is expected.   
  2. **Download Anyplace v3:**
        $ wget https://anyplace.cs.ucy.ac.cy/downloads/anyplace_v3.zip  
        #if you don't have wget, just download the file with a browser)
    
