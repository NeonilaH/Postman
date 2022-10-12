## HW_2 Postman

### Create requests in Postman.

###### Protocol: http
###### IP: 162.55.220.72
###### Port: 5005

### EP_1
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

### EP_2
###### Method: POST
###### EndPoint: /user_info_3
###### request form data: 
######  name: str
######  age: int
######  salary: int

#### Response:
```json
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}
                     }
```                     
![image](https://user-images.githubusercontent.com/106426661/174314474-a5fd30d1-fc03-41a5-8abd-1b9ff1d34751.png)


### EP_3
###### Method: GET
###### EndPoint: /object_info_1
###### request url params: 
######  name: str
######  age: int
######  weight: int

#### Response:  
```json
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```         
          
![image](https://user-images.githubusercontent.com/106426661/174316921-8678c0e6-1c6b-496f-87b1-c743c7d3bc21.png)

### EP_4
###### Method: GET
###### EndPoint: /object_info_2
###### request url params: 
######  name: str
######  age: int
######  salary: int

#### Response:  
```
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```
          
![image](https://user-images.githubusercontent.com/106426661/174318984-eb24a3bd-5e3d-45a7-a177-bed2711cb34a.png)

### EP_5
###### Method: GET
###### EndPoint: /object_info_3
###### request url params: 
######  name: str
######  age: int
######  salary: int

#### Response:  
```
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }

```
![image](https://user-images.githubusercontent.com/106426661/174319778-592aee2b-1d74-447b-9000-a8cb37db831e.png)

### EP_6
###### Method: GET
###### EndPoint: /object_info_4
###### request url params: 
######  name: str
######  age: int
######  salary: int

#### Response:
```
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
```

![image](https://user-images.githubusercontent.com/106426661/174320524-863490f4-4927-4992-896a-4b9dbf821990.png)

### EP_7
###### Method: POST
###### EndPoint: /user_info_2
###### request form data: 
######  name: str
######  age: int
######  salary: int

#### Response:  
```
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
 ```
![image](https://user-images.githubusercontent.com/106426661/174322268-c7f790b1-9557-48f5-82b2-3b251da91dba.png)

### Run collection

![image](https://user-images.githubusercontent.com/106426661/174355822-a0084834-3291-47bc-840d-9aa2363b2dae.png)

