## HW_2 Postman

### Method `GET`,  URL `http://162.55.220.72:5005/first`

#### 1. Submit the request.

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

### Method `GET`,  URL `http://162.55.220.72:5005/object_info_3`

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
    "name": "Nelly",
    "salary": 1000
}
```

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
pm.test("Response name = Request name", () => {
    pm.expect(resp.name).to.eql(req.name)
});
```

#### 6. Check that the age in the response is equal to the age in the request (take the age from the request).

```js
pm.test("Response age = Request age", () => {
    pm.expect(resp.age).to.eql(req.age)
});
```

#### 7. Check that the salary in the response is equal to the salary in the request (pick the salary from the request).

```js
pm.test("Response salary = Request salary", () => {
    pm.expect(resp.salary).to.eql(+req.salary)
});
```

#### 8. Print the family parameter from the response to the console.

```js
pm.test("Console family response", () => {
    console.log(resp.family)
});
```

#### 9. Check that the dog parameter has name parameters.

```js
pm.test("Dog has name", () => {
    pm.expect(resp.family.pets.dog).haveOwnProperty("name")
});
```

#### 10. Check that the dog parameter has age parameters.

```js
pm.test("Dog has age", () => {
    pm.expect(resp.family.pets.dog).haveOwnProperty("age")
});
```

#### 11. Check that the name parameter is set to Luky.

```js
pm.test("Dog name has value Luky", () => {
    pm.expect(resp.family.pets.dog.name).to.eql("Luky");
});
```

#### 12. Check that the age parameter is 4.

```js
pm.test("Dog age has value 4", () => {
    pm.expect(resp.family.pets.dog.age).to.eql(4);
});
```

***

### Method `GET`,  URL `http://162.55.220.72:5005/object_info_4`

#### 1. Submit a request.

The response
```json
{
    "age": 35,
    "name": "Nelly",
    "salary": [
        1000,
        "2000",
        "3000"
    ]
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
let resp = pm.response.json();  
```

#### 4. Parse the request.

```js
let req = pm.request.url.query.toObject();
```

#### 5. Check that the name in the response is equal to the name in the request (take the name from the request).

```js
pm.test("Response name = Request name", () => {
    pm.expect(resp.name).to.eql(req.name)
});
```

#### 6. Check that the age in the response is equal to the age in the request (take the age from the request).

```js
pm.test("Response age = Request age", () => {
    pm.expect(resp.age).to.eql(req.age)
});
```

#### 7. Print the salary parameter from request to the console.

```js
pm.test("Console salary request", () => {
    console.log(req.salary)
});
```

#### 8. Print the salary parameter from the response to the console.

```js
pm.test("Console salary response", () => {
    console.log(resp.salary)
});
```

#### 9. Print the 0th element of the salary parameter from response to the console.

```js
pm.test("The 0th element of the salary", () => {
    console.log("the 0th element of the salary is ", resp.salary)
});
```

#### 10. Print to the console the 1st element of the salary parameter, the salary parameter from the response.

```js
pm.test("The 1th element of the salary", () => {
    console.log("the 1st element of the salary is " + resp.salary[1])
});
```

#### 11. Print to the console the 2nd element of the salary parameter, the salary parameter from the response.

```js
pm.test("The 2nd element of the salary", () => {
    console.log("the 2nd element of the salary is " + resp.salary[2])
});
```

#### 12. Check that the 0th element of the salary parameter is equal to the salary from the request (pick the salary from the request).

```js
pm.test("Response salary[0] = Request salary", () => {
    pm.expect(resp.salary[0]).to.eql(+req.salary)
});
```

#### 13. Check that the 1st element of the salary parameter is equal to the salary*2 from the request (pick the salary from the request).

```js
pm.test("Response salary[1] = Request salary * 2", () => {
    pm.expect(+resp.salary[1]).to.eql(+req.salary * 2)
});
```

#### 14. Check that the 2nd element of the salary parameter is equal to the salary*3 from the request (pick the salary from the request).

```js
pm.test("Response salary[2] = Request salary * 3", () => {
    pm.expect(+resp.salary[2]).to.eql(+req.salary * 3)
});
```

