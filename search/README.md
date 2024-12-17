

-------------------------------------------------------

** Experimental syntax for search queries ** (using the same backend implementation)

> curl -i http://localhost:5003/v1/people-search/?access_token=a0fe2f40415f7451c4ba2eae7da963d5&full-name=Muneeb Ali
> curl -i http://localhost:5003/v1/people-search/?access_token=a0fe2f40415f7451c4ba2eae7da963d5&twitter=ryaneshea
	
> curl -i http://localhost:5003/v1/people-search/?access_token=a0fe2f40415f7451c4ba2eae7da963d5&btc_address=1G6pazv8zjWKBWouXVgHHvgmRmSm7JmH3S

### 3) Profile API (powered by mongodb)


Request parameters: 

> access_token and onenameID

Syntax: 

> {machine_ip}/v1/people/?id={onename_id}&access_token={access_token}

EXAMPLE:
	
> curl -G http://localhost:5003/v1/people/ -d "onename_id=muneeb&access_token=a0fe2f40415f7451c4ba2eae7da963d5"

----------------------------------------------
old Notes (to be deprecated):
----------------------------------------------


We currently have two search sub-systems to handle search queries:

* Substring search on people names (just from full_name of people)
* Search on the raw lucene index (build from entire OneName profiles)



     {
          "query": "the search query/term",
          "limit_results": "numeric limit on number of results e.g., 50, this parameter is optional"
     }

The API returns a JSON object of the format:

     {
          "people": [ ]
     }

### Quick Testing

You can test the search API using curl:

> curl http://server_ip>/<path_to_api_endpoint> -G -d "query=fred%20wilson"

OR by using the [test_client.py](test_client.py)

> ./test_client.py "fred wilson"

Make sure that the packages listed in requirements.txt are installed before using the test_client.py

This will currently return upto a max of 20 results (can be less depending on the query) with data that follows structure of OneName profiles described here:

https://github.com/onenameio/onename
