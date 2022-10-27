# Postman
## HW_1 Postman

### Create requests in Postman.

[Request_1.1](#1.1)  
[Request_1.2](#1.2)   
[Request_1.3](#1.3)     
[Request_1.4](#1.4)     
[Request_1.5](#1.5)     
[Request_1.6](#1.6)     
[Request_1.7](#1.7)
[Run collection_1.8](#1.8)

###### Protocol: http
###### IP: 162.55.220.72
###### Port: 5005

***
## **Request_1.1**<a name="1.1"><a>
    
###### Method: GET
###### EndPoint: /get_method
###### request url params: 
######  name: str
######  age: int

#### Response: 
```json
[
    "Neonila",
    "34"
]
```

## **Request_1.2**<a name="1.2"><a>
    
###### Method: POST
###### EndPoint: /user_info_3
###### request form data: 
######  name: str
######  age: int
######  salary: int

#### Response:
```json
{
    "age": "34",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "u_salary_1_5_year": 4000
    },
    "name": "Neonila",
    "salary": 1000
}
```                     


## **Request_1.3**<a name="1.3"><a>
    
###### Method: GET
###### EndPoint: /object_info_1
###### request url params: 
######  name: str
######  age: int
######  weight: int

#### Response:  
```json
{
    "age": 34,
    "daily_food": 0.744,
    "daily_sleep": 155.0,
    "name": "Neonila"
}
```         
          

## **Request_1.4**<a name="1.4"><a>
    
###### Method: GET
###### EndPoint: /object_info_2
###### request url params: 
######  name: str
######  age: int
######  salary: int

#### Response:  
```json
{
    "person": {
        "u_age": 34,
        "u_name": [
            "Neonila",
            1000,
            34
        ],
        "u_salary_5_years": 4200.0
    },
    "qa_salary_after_1.5_year": 3300.0,
    "qa_salary_after_12_months": 2700.0,
    "qa_salary_after_3.5_years": 3800.0,
    "qa_salary_after_6_months": 2000,
    "start_qa_salary": 1000
}
``` 
          

## **Request_1.5**<a name="1.5"><a>
    
###### Method: GET
###### EndPoint: /object_info_3
###### request url params: 
######  name: str
######  age: int
######  salary: int

#### Response:  
```json
{
    "age": "34",
    "family": {
        "children": [
            [
                "Alex",
                24
            ],
            [
                "Kate",
                12
            ]
        ],
        "pets": {
            "cat": {
                "age": 3,
                "name": "Sunny"
            },
            "dog": {
                "age": 4,
                "name": "Luky"
            }
        },
        "u_salary_1_5_year": 4000
    },
    "name": "Neonila",
    "salary": 1000
}
```

## **Request_1.6**<a name="1.6"><a>
    
###### Method: GET
###### EndPoint: /object_info_4
###### request url params: 
######  name: str
######  age: int
######  salary: int

#### Response:
```json
{
    "age": 34,
    "name": "Neonila",
    "salary": [
        1000,
        "2000",
        "3000"
    ]
}
```


## **Request_1.7**<a name="1.7"><a>
    
###### Method: POST
###### EndPoint: /user_info_2
###### request form data: 
######  name: str
######  age: int
######  salary: int

#### Response:  
```json
{
    "person": {
        "u_age": 34,
        "u_name": [
            "Neonila",
            1000,
            34
        ],
        "u_salary_5_years": 4200.0
    },
    "qa_salary_after_1.5_year": 3300.0,
    "qa_salary_after_12_months": 2700.0,
    "qa_salary_after_3.5_years": 3800.0,
    "qa_salary_after_6_months": 2000,
    "start_qa_salary": 1000
}
 ```

## **Run collection_1.8**<a name="1.8"><a>

![image](https://user-images.githubusercontent.com/106426661/174355822-a0084834-3291-47bc-840d-9aa2363b2dae.png)
