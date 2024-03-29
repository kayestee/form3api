# Form3 Sample client execution code
This is my first Go program. This is a sample project that is used to test form3 client API library.
https://github.com/kayestee/f3_client.
Clone the project to your local. 
git clone https://github.com/kayestee/form3interviewapi.git



## Running in docker
To run the form3 client in docker execute the docker-compose command inside the docker folder.

``` docker-compose -f docker-compose.yml up ```

The tests results will be logged to the console log. 
Note: During the first docker compose run some tests may fail because the form3 accountapi is not ready yet. 
In which case, please re-run the compose command. 

## API's list
* The sample go file uses go test package to demonstrate the form3 client API endpoints Create, Fetch and Delete.

* The test results are logged to the console. This sample just prints each test result as they are run and not a report. 

* Here is a sample JSON for create API request:
``` {
  "data": {
    "id": "{{random_guid}}",
    "organisation_id": "{{organisation_id}}",
    "type": "accounts",
    "attributes": {
       "country": "GB",
        "base_currency": "GBP",
        "bank_id": "400302",
        "bank_id_code": "GBDSC",
        "account_number": "10000004",
        "customer_id": "234",
        "iban": "GB28NWBK40030212764204",
        "bic": "NWBKGB42",
        "account_classification": "personal",
        "name" : ["Test Account"]
    }
  }
}
```

Fetch and Delete uses the account Id created from the above create API call.

Reference:: https://www.api-docs.form3.tech/api/tutorials/getting-started/create-an-account/bank-accounts-at-form3
