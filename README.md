Postman.
HW_1

Создать запросы в Postman.

Protocol: http
IP: 162.55.220.72
Port: 5005

EP_1
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
]
![image](https://user-images.githubusercontent.com/106426661/174310954-605185ce-c530-4e27-b313-37cbcb49e951.png)

EP_2
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
![image](https://user-images.githubusercontent.com/106426661/174314474-a5fd30d1-fc03-41a5-8abd-1b9ff1d34751.png)
