## HW_2 Postman

### Method `GET`,  URL `http://162.55.220.72:5005/first`

#### 1. Submit the request.

The response
```
This is the first responce from server!  
```

#### 2. Status code 200

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

### Method `POST`,  URL `http://162.55.220.72:5005/user_info_3`

#### 1. Submit the request.

The response
```json
{
    "age": "35",
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
    "name": "Nelly",
    "salary": 1000
}
```

#### 2. Status code 200

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Parse the response body into json.

```js
let responseData = pm.response.json();  
console.log('Response data:', responseData);
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
pm.test("Your test salary", () => {
    pm.expect(responseData.salary).to.eql(1000);
});
```

#### 7. Parse the request.

```js
let req = request.data
```

#### 8. Check that the name in the response is equal to the name in the request (take the name from the request.)

```js
pm.test("Response name = Request name", function () {
    pm.expect(responseData.name).to.eql(req.name);
});
```

#### 9. Check that the age in the response is equal to the age in the request (take the age from the request.)

```js
pm.test("Response age = Request age", () => {
    pm.expect(responseData.age).to.eql(req.age);
});
```

#### 10. Check that the salary in the response is equal to the salary in the request (pick the salary from the request.)

```js
pm.test("Response salary = Request salary", () => {
    pm.expect(responseData.salary).to.eql(+req.salary);
});
```

#### 11. Print the family parameter from response to the console.

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
