# Form3 Sample client execution code
This is just a sample project that is used to sample possible API endpoints for form3 client API library.
https://github.com/kayestee/f3_client.
Clone the project to your local. 
git clone https://github.com/kayestee/form3interviewapi.git


## Instructions
Include github.com/kayestee/f3_client in your go.mod file as require dependencies.
And run below to get the latest client API. 
go mod tidy 

### Running in docker
To run the sampleclient folder in docker execute the docker-compose command inside docker folder.

``` docker-compose -f docker-compose.yml up ```

The tests results will be wriiten to the console log. 

## API's list
The sample go file uses go test package to demonstrate the form3 client API.

Here is a sample JSON for create API request:
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

Fetch and Delete uses the account Id created from the above API call.

Reference:: https://www.api-docs.form3.tech/api/tutorials/getting-started/send-a-payment/create-the-payment
