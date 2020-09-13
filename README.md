### Table of Contents

1. [Overview](#Overview)
2. [Getting-Started](#Getting-Started)
3. [Description](#Description)
4. [Approach](#Approach)
5. [Usage](#Usage)
6. [Limitation](#Limitation)
7. [License](#License)

### Overview

* This code demonstrates how to retreive data for different input parameter combinations (square meter and zip code) in an automated way.
As in this case scenario we are retreiving prices from ![Friday](https://hausratversicherung.friday.de/offer) using python.


### Getting-Started

1. Prerequisites:

* The requirement for this Python project . You need to have Python (3.6 version  & above recommended) 


### Description 

* It takes the input from user i.e. area in sq.m & postal code and returns the insurance prices by passing those values
through the following hosted ![api](https://fdy2-policycenter-production.k8s.blue.friday-prod.de/rest/friday/hc/price?) 


### Approach

* Getting the api url from Google Console.
![Chrome_Console](https://github.com/himani-de/python-requests/blob/master/images/chrome_console.png)

* Checking the response on chrome console
![Cheome_Resonse](https://github.com/himani-de/python-requests/blob/master/images/chrome_response.png)

* Testing the parameters in Postman
![Postman_Parameters](https://github.com/himani-de/python-requests/blob/master/images/postman_get.png)

* Checking the max area limit that can be insured
![Area_Limit](https://github.com/himani-de/python-requests/blob/master/images/area_limit.png)



### Usage

* Based on the above approach analysis the area limit has been validated and handled in the code.

Run the code
```
python python_request.ipynb
Please enter the area:
23
Please enter the postal code:
60306
postal_code 60306

```

Following prices is retreived.

```
{"additionalCoverages":{"coverages":[{"code":"HcAllRiskCov_Fdy","insuredSum":{"amount":14950.0,"currency":"EUR"},"optional":true,"price":{"amount":1.19,"currency":"EUR"}},{"code":"HcExtBikeCov_Fdy","insuredSum":{"amount":1000.0,"currency":"EUR"},"optional":true,"price":{"amount":2.62,"currency":"EUR"}},{"code":"HcGlassCov_Fdy","insuredSum":{"amount":14950.0,"currency":"EUR"},"optional":true,"price":{"amount":0.63,"currency":"EUR"}},{"code":"HcNatHazardCov_Fdy","insuredSum":{"amount":14950.0,"currency":"EUR"},"optional":true,"price":{"amount":2.52,"currency":"EUR"}}],"price":{"amount":6.96,"currency":"EUR"}},"basicCoverages":{"coverages":[{"code":"HcBasicCov_Fdy","insuredSum":{"amount":14950.0,"currency":"EUR"},"optional":false,"price":{"amount":1.79,"currency":"EUR"},"priceBeforeDiscounts":{"amount":1.7,"currency":"EUR"}}],"price":{"amount":1.79,"currency":"EUR"},"priceBeforeDiscounts":{"amount":1.7,"currency":"EUR"}}}
```  

### Limitation 

 
This code has been tested on following Python Version. 

* Python 3.7.3

### License

Released under MIT license, see [LICENSE](LICENSE.md) for details.
