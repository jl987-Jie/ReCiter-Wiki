##Report: Results of eSearch query
esearchResults contains the PubMed query constructed by ReCiter, number of articles returned for each query, retrieval strategy used and the date of retrieval.

```json```
{  
      "cwid":"wcb2001",
      "pubMedQueryResults":[  
         {  
            "query":"wcb2001@med.cornell.edu", // query used to retrieve
            "numResult":2, // number of results
            "used":true // was this query used (since ReCiter used two different types of queries, one with first name and another with first initial, we need a boolean to decide which one was used. However, this does not apply to email queries).
         },
         {  
            "query":"wcb2001@med.cornell.edu",
            "numResult":0,
            "used":false
         }
      ],
      "esearchPmid":{  
         "pmids":[  // pmids retrieved using email strategy
            11381530,
            15465317
         ],
         "retrievalStrategyName":"EmailRetrievalStrategy",
         "retrievalDate":{  // retrieval date
            "dayOfYear":332,
            "dayOfWeek":"SUNDAY",
            "dayOfMonth":27,
            "monthValue":11,
            "year":2016,
            "month":"NOVEMBER",
            "hour":15,
            "minute":27,
            "second":35,
            "nano":338000000,
            "chronology":{  
               "calendarType":"iso8601",
               "id":"ISO"
            }
         }
      }
   }
```