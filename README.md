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
>  Nov 21,2017 23:45.


[Research paper for Indoor positioning System](http://www.sigspatial.org/sigspatial-special-issues/sigspatial-special-volume-9-number-2-july-2017/04-Paper01_Anatomy.pdf)

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
    
        $ unzip anyplace_v3.zip
        #if you don't have unzip, just use any unzip tool (winzip, etc.)
 
    
3. **Configure Couchbase to connect to AnyPlace** Now you have to change the default configurations. Please follow the below instructions before running Anyplace
        
    + Fill in the parameters in `conf/application.conf` file 
        * `application.secret="Iamawesome123"`
            ```
            couchbase.hostname="http://localhost/anyplace_db_1"
            couchbase.port=8091
            couchbase.bucket="anyplace"
            couchbase.username="o"
            couchbase.password="ada"
            ```
    
    + Make sure a Couchbase instance is running, with the [Production Views](https://developer.couchbase.com/documentation/server/4.6/introduction/whats-new.html) the server invokes.
    You can use the automated script (`create-views.sh`) in order to create the views under the [`anyplace_views`](https://github.com/piyushimraw/anyplace/tree/master/server/anyplace_views) directory.
    You need to set the username and the password for your couchbase instance.  
        * `USERNAME="o"` - This is the administrator's username for the couchbase instance.
        * `PASSWORD="ada"` - This is the administrator's password for the couchbase instance.
        * `BUCKET="anyplace"` - This is the bucket for the couchbase instance.

    ***Running The server***
                
                # WINDOWS
                $ Go to the folder you unzipped in the prior step, then go to "bin" 
                $ Double click  anyplace_v3.bat
                # To stop press Ctrl-C or kill the respective process through the task manager
                
                
 ## TEST THIS ON ANDOROID
   
   ```
   {
   "num_of_pois": 7,
   "pois": 
       [
             {
               "lat": "37.719272447256486",
               "lon": "-97.29351036250591",
               "puid": "poi_9d376468-a48d-405e-adba-d464de071438",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "Other"
             },
             {
               "lat": "37.71928305563099",
               "lon": "-97.29349695146084",
               "puid": "poi_237dcff7-9262-4a8d-8f2d-6bf6a8f8349c",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "None"
             },
             {
               "lat": "37.71928623814301",
               "lon": "-97.29344196617603",
               "puid": "poi_55b769d7-0b31-45ad-b488-c3078dd90101",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "None"
             },
             {
               "lat": "37.71928570772435",
               "lon": "-97.29340374469757",
               "puid": "poi_5318c209-c094-406e-ac34-183a7d1948aa",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "None"
             },
             {
               "lat": "37.719284646887026",
               "lon": "-97.29337491095066",
               "puid": "poi_0ea97e68-8726-453d-817d-841bb200cac5",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "None"
             },
             {
               "lat": "37.7193159415822",
               "lon": "-97.29337625205517",
               "puid": "poi_e9203073-c3f4-4f87-9c55-9dfdea40e903",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "None"
             },
             {
               "lat": "37.719322306603345",
               "lon": "-97.29334004223347",
               "puid": "poi_1197c54c-7e83-4a96-89d8-8ffcbcc63b67",
               "buid": "building_b4e7a3ea-99e0-4102-b1f6-bd7a1cde66fc_1476898501463",
               "floor_number": "2",
               "pois_type": "Room"
             }
       ],
   "status": "success",
   "message": "Successfully plotted navigation.",
   "status_code": 200
 }
   ```
