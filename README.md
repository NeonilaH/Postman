####  HW_1 Postman

[Request_1.1](#1.1)  
[Request_1.2](#1.2)   
[Request_1.3](#1.3)     
[Request_1.4](#1.4)     
[Request_1.5](#1.5)     
[Request_1.6](#1.6)     
[Request_1.7](#1.7)</br>
[Run collection_1.8](#1.8)

####  HW_2 Postman

[Autotests_2.1](#2.1)  
[Autotests_2.2](#2.2)   
[Autotests_2.3](#2.3)     
[Autotests_&_Environments_2.4](#2.4)     
[Autotests_&_Environments_2.5](#2.5) 

***

## HW_1 Postman

### Create requests in Postman.
Protocol: http</br>
IP: 162.55.220.72</br>
Port: 5005

## **Request_1.1**<a name="1.1"><a>
    
Method: GET</br>
EndPoint: /get_method</br>
request url params: </br>
name: str</br>
age: int</br>

#### Response: 
```json
[
    "Neonila",
    "34"
]
```

## **Request_1.2**<a name="1.2"><a>
    
Method: POST</br>
EndPoint: /user_info_3</br>
request form data: </br>
name: str</br>
age: int</br>
salary: int</br>

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
    
Method: GET</br>
EndPoint: /object_info_1</br>
request url params: </br>
name: str</br>
age: int</br>
weight: int

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
    
Method: GET</br>
EndPoint: /object_info_2</br>
request url params:</br> 
name: str</br>
age: int</br>
salary: int

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
    
Method: GET</br>
EndPoint: /object_info_3</br>
request url params: </br>
name: str</br>
age: int</br>
salary: int

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
    
Method: GET</br>
EndPoint: /object_info_4</br>
request url params: </br>
name: str</br>
age: int</br>
salary: int

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
    
Method: POST</br>
EndPoint: /user_info_2</br>
request form data: </br>
name: str</br>
age: int</br>
salary: int

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

***	

## HW_2 Postman

## **Autotests_2.1**<a name="2.1"><a>

#### 1. Submit the request.

Method `GET`,  URL `http://162.55.220.72:5005/first`	
	
The response
```
This is the first responce from server!  
```

#### 2. Status code 200.

Choose the `Status code: Code is 200` snippet
```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Check that the correct string comes in the body.

```js
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server!")
    })
```

***	
	
## **Autotests_2.2**<a name="2.2"><a>	

#### 1. Submit the request.
Method `POST`,  URL `http://162.55.220.72:5005/user_info_3`

#### 2. Status code 200.

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Parse the response body into json.

```js
let responseData = pm.response.json();  
```

#### 4. Check that the name in the response is equal to the name in the request (type the name manually).

```js
pm.test("Your test name", function () {
    pm.expect(responseData.name).to.eql('Nelly');
});
```

#### 5. Check that the age in the response is equal to the age in the request (type the age manually).

```js
pm.test("Your test age", function () {
    pm.expect(responseData.age).to.eql('35');
});
```

#### 6. Check that the salary in the response is equal to the salary in the request (type the salary manually).

```js
pm.test("Your test salary", function () {
    pm.expect(responseData.salary).to.eql(1000);
});
```

#### 7. Parse the request.

```js
let req = request.data
```

#### 8. Check that the name in the response is equal to the name in the request (take the name from the request).

```js
pm.test("Response name = Request name", function () {
    pm.expect(responseData.name).to.eql(req.name);
});
```

#### 9. Check that the age in the response is equal to the age in the request (take the age from the request).

```js
pm.test("Response age = Request age", function () {
    pm.expect(responseData.age).to.eql(req.age);
});
```

#### 10. Check that the salary in the response is equal to the salary in the request (pick the salary from the request).

```js
pm.test("Response salary = Request salary", function () {
    pm.expect(responseData.salary).to.eql(+req.salary);
});
```

#### 11. Print the family parameter from the response to the console.

```js
pm.test("Console family response", function () {
    console.log(responseData.family)
});
```

#### 12. Check that u_salary_1_5_year in the response is equal to the salary * 4 (pick the salary from the request).

```js
pm.test("Salary * 4 in 1.5 years", function () {    
    pm.expect(responseData.family.u_salary_1_5_year).to.eql(4 * req.salary);
});
```

***

## **Autotests_2.3**<a name="2.3"><a>

#### 1. Submit the request.

Method `GET`,  URL `http://162.55.220.72:5005/object_info_3`
	
#### 2. Status code 200.

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Parse the response body into json.

```js
let resp = pm.response.json();  
```

#### 4. Parse the request.

```js
let req = pm.request.url.query.toObject();
```

#### 5. Check that the name in the response is equal to the name in the request (take the name from the request).

```js
pm.test("Response name = Request name", function () {
    pm.expect(resp.name).to.eql(req.name)
});
```

#### 6. Check that the age in the response is equal to the age in the request (take the age from the request).

```js
pm.test("Response age = Request age", function () {
    pm.expect(resp.age).to.eql(req.age)
});
```

#### 7. Check that the salary in the response is equal to the salary in the request (pick the salary from the request).

```js
pm.test("Response salary = Request salary", function () {
    pm.expect(resp.salary).to.eql(+req.salary)
});
```

#### 8. Print the family parameter from the response to the console.

```js
pm.test("Console family response", function () {
    console.log(resp.family)
});
```

#### 9. Check that the dog parameter has name parameters.

```js
pm.test("Dog has name", function () {
    pm.expect(resp.family.pets.dog).haveOwnProperty("name")
});
```

#### 10. Check that the dog parameter has age parameters.

```js
pm.test("Dog has age", function () {
    pm.expect(resp.family.pets.dog).haveOwnProperty("age")
});
```

#### 11. Check that the name parameter is set to Luky.

```js
pm.test("Dog name has value Luky", function () {
    pm.expect(resp.family.pets.dog.name).to.eql("Luky");
});
```

#### 12. Check that the age parameter is 4.

```js
pm.test("Dog age has value 4", function () {
    pm.expect(resp.family.pets.dog.age).to.eql(4);
});
```

***

## **Autotests_&_Environments_2.4**<a name="2.4"><a>	

#### 1. Submit a request.

Method `GET`,  URL `http://162.55.220.72:5005/object_info_4`	

#### 2. Status code 200.

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Parse the response body into json.

```js
let resp = pm.response.json();  
```

#### 4. Parse the request.

```js
let req = pm.request.url.query.toObject();
```

#### 5. Check that the name in the response is equal to the name in the request (take the name from the request).

```js
pm.test("Response name = Request name", function () {
    pm.expect(resp.name).to.eql(req.name)
});
```

#### 6. Check that the age in the response is equal to the age in the request (take the age from the request).

```js
pm.test("Response age = Request age", function () {
    pm.expect(resp.age).to.eql(req.age)
});
```

#### 7. Print the salary parameter from request to the console.

```js
pm.test("Console salary request", function () {
    console.log(req.salary)
});
```

#### 8. Print the salary parameter from response to the console.

```js
pm.test("Console salary response", function () {
    console.log(resp.salary)
});
```

#### 9. Print the 0th element of the salary parameter from response to the console.

```js
pm.test("The 0th element of the salary", function () {
    console.log("the 0th element of the salary is ", resp.salary)
});
```

#### 10. Print to the console the 1st element of the salary parameter, the salary parameter from the response.

```js
pm.test("The 1th element of the salary", function () {
    console.log("the 1st element of the salary is " + resp.salary[1])
});
```

#### 11. Print to the console the 2nd element of the salary parameter, the salary parameter from the response.

```js
pm.test("The 2nd element of the salary", function () {
    console.log("the 2nd element of the salary is " + resp.salary[2])
});
```

#### 12. Check that the 0th element of the salary parameter is equal to the salary from the request (pick the salary from the request).

```js
pm.test("Response salary[0] = Request salary", function () {
    pm.expect(resp.salary[0]).to.eql(+req.salary)
});
```

#### 13. Check that the 1st element of the salary parameter is equal to the salary*2 from the request (pick the salary from the request).

```js
pm.test("Response salary[1] = Request salary * 2", function () {
    pm.expect(+resp.salary[1]).to.eql(+req.salary * 2)
});
```

#### 14. Check that the 2nd element of the salary parameter is equal to the salary*3 from the request (pick the salary from the request).

```js
pm.test("Response salary[2] = Request salary * 3", function () {
    pm.expect(+resp.salary[2]).to.eql(+req.salary * 3)
});
```

#### 15. Create a variable name in the environment.

After clicking New button at top right, choose Environment and give it a name. 
In the Environment add variable `name` and set value `Nelly`.

#### 16. Create a variable age in the environment.

In the Environment add variable `age` and set value `35`. 


#### 17. Create a salary variable in the environment

In the Environment add variable `salary` and set value `1000`. 

#### 18. Pass the name variable to the environment.

```js
let name = req.name
pm.environment.set("name", name);
```

#### 19. Pass the age variable to the environment.

```js
let age = req.age
pm.environment.set("age", age);
```

#### 20. Pass the salary variable to the environment

```js
let salary = req.salary
pm.environment.set("salary", salary);
```

#### 21. Write a loop that will output the list elements from the salary parameter to the console in order.

```js
for (let i = 0; i < resp.salary.length ; i++) {
console.log(resp.salary[i])
};
```

***

## **Autotests_&_Environments_2.5**<a name="2.5"><a>				      

#### 1. Insert the salary parameter from the environment into the request.
In Body tab choose form-data. Set KEY `salary` and VALUE `{{salary}}`.

#### 2. Insert the age parameter from the environment into age.
In Body tab choose form-data. Set KEY `age` and VALUE `{{age}}`.

#### 3. Insert the name parameter from the environment into name.
In Body tab choose form-data. Set KEY `name` and VALUE `{{name}}`.

#### 4. Submit the request.
Method `POST`,  URL `hhttp://162.55.220.72:5005/user_info_2`

#### 5. Status code 200.

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 6. Parse the response body to json.

```js
let resp = pm.response.json();
```

#### 7. Parse the request.

```js
let req = request.data;
```

#### 8. Check json response has start_qa_salary parameter.

```js
pm.test("start_qa_salary in response", function () {
    pm.expect(resp).to.haveOwnProperty("start_qa_salary")
});
```

#### 9. Check json response has qa_salary_after_6_months parameter.

```js
pm.test("qa_salary_after_6_months in response", function () {
    pm.expect(resp).to.haveOwnProperty("qa_salary_after_6_months")
});
```

#### 10. Check json response has qa_salary_after_12_months parameter.

```js
pm.test ("qa_salary_after_12_months in response", function () {
    pm.expect(resp).to.haveOwnProperty("qa_salary_after_12_months")
});
```

#### 11. Check json response has qa_salary_after_1.5_year parameter.

```js
pm.test ("qa_salary_after_1.5_year in response", function () {
    pm.expect(resp).to.haveOwnProperty("qa_salary_after_1.5_year")
});
```

#### 12. Check json response has qa_salary_after_3.5_years parameter.

```js
pm.test ("qa_salary_after_3.5_years in response", function () {
    pm.expect(resp).to.haveOwnProperty("qa_salary_after_3.5_years")
});
```

#### 13. Check json response has person parameter.

```js
pm.test ("person in response", function () {
    pm.expect(resp).to.haveOwnProperty("person")
});
```
#### 14. Check that the start_qa_salary parameter is equal to the salary from the request (take the salary from the request).

```js
pm.test ("start_qa_salary = salary from the request", function () {
    pm.expect(resp.start_qa_salary).to.eql(+req.salary)
});
```

#### 15. Check that the qa_salary_after_6_months parameter is equal to salary*2 from the request (take the salary from the request).

```js
pm.test ("qa_salary_after_6_months = salary*2 from the request", function () {
    pm.expect(resp.qa_salary_after_6_months).to.eql(req.salary*2)
});
```

#### 16. Check that the qa_salary_after_12_months parameter is equal to salary*2.7 from the request (take the salary from the request).

```js
pm.test ("qa_salary_after_12_months = salary*2.7 from the request", function () {
    pm.expect(resp.qa_salary_after_12_months).to.eql(+req.salary*2.7)
});
```

#### 17. Check that the qa_salary_after_1.5_year parameter is equal to salary*3.3 from the request (take the salary from the request).

```js
pm.test ("qa_salary_after_1.5_year = salary*3.3 from the request", function () {
    pm.expect(resp['qa_salary_after_1.5_year']).to.eql(+req.salary*3.3)
});
```

#### 18. Check that the qa_salary_after_3.5_years parameter is equal to salary*3.8 from the request (take the salary from the request).

```js
pm.test ("qa_salary_after_3.5_year = salary*3.8 from the request", function () {
    pm.expect(resp['qa_salary_after_3.5_years']).to.eql(+req.salary*3.8)
});
```

#### 19. Check that in the person parameter, the 1st element from u_name is equal to salary from the request (take the salary from the request).

```js
pm.test("response u_name[1] = request salary", function () {
    pm.expect(resp.person.u_name[1]).to.eql(+req.salary);
});
```

#### 20. Check that the u_age parameter is equal to age from  the request (take the salary from the request).

```js
pm.test("response u_age = request age", function () {
    pm.expect(resp.person.u_age).to.eql(+req.age);
});
```

#### 21. Check that the u_salary_5_years parameter is equal to salary*4.2 from  the request (take the salary from the request).

```js
pm.test ("u_salary_5_years = salary*4.2 from the request", function () {
    pm.expect(resp.person.u_salary_5_years).to.eql(+req.salary*4.2)
});
```

#### 22. ***Write a loop that will output the list items from the person parameter to the console in order.

```js
for (let i in resp.person) {  
console.log(i +': ' + resp.person[i]);  
	};
```

Console:
```
u_age: 35
u_name: Nelly,1000,35
u_salary_5_years: 4200
```
