## HW_2 Postman

### Create requests in Postman.

[Request_1](#1.1)  
[Request_2](#1.2)   
[Request_3](#1.3)     
[Request_4](#1.4)     
[Request_5](#1.5)     
[Request_6](#1.6)     
[Request_7](#1.7)  

###### Protocol: http
###### IP: 162.55.220.72
###### Port: 5005

***
## **Request_1**<a name="1.1"><a>
    
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
![image](https://user-images.githubusercontent.com/106426661/174310954-605185ce-c530-4e27-b313-37cbcb49e951.png)

## **Request_2**<a name="1.2"><a>
    
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
![image](https://user-images.githubusercontent.com/106426661/174314474-a5fd30d1-fc03-41a5-8abd-1b9ff1d34751.png)


## **Request_3**<a name="1.3"><a>
    
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
          
![image](https://user-images.githubusercontent.com/106426661/174316921-8678c0e6-1c6b-496f-87b1-c743c7d3bc21.png)

## **Request_4**<a name="1.4"><a>
    
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
          
![image](https://user-images.githubusercontent.com/106426661/174318984-eb24a3bd-5e3d-45a7-a177-bed2711cb34a.png)

## **Request_5**<a name="1.5"><a>
    
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
![image](https://user-images.githubusercontent.com/106426661/174319778-592aee2b-1d74-447b-9000-a8cb37db831e.png)

## **Request_6**<a name="1.6"><a>
    
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

![image](https://user-images.githubusercontent.com/106426661/174320524-863490f4-4927-4992-896a-4b9dbf821990.png)

## **Request_7**<a name="1.7"><a>
    
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
![image](https://user-images.githubusercontent.com/106426661/174322268-c7f790b1-9557-48f5-82b2-3b251da91dba.png)

### Run collection

![image](https://user-images.githubusercontent.com/106426661/174355822-a0084834-3291-47bc-840d-9aa2363b2dae.png)

