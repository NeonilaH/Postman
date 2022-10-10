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
pm.test("Your test body", function () {
    pm.response.to.have.body('This is the first responce from server!');
});
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

Choose the `Status code: Code is 200` snippet
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

#### 4. Check that the name in the response is equal to the name in the request (type the name manually.)

```js
pm.test("Your test name", function () {
    pm.expect(responseData.name).to.eql('Nelly');
});
```

#### 5. Check that the age in the response is equal to the age in the request (type the age manually.)


```js
pm.test("Your test age", function () {
    pm.expect(responseData.age).to.eql('35');
});
```

#### 6. 
