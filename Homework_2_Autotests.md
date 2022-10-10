## HW_2 Postman

### Method `GET`,  URL `http://162.55.220.72:5005/first`

#### 1. Submit a request.

Response
```
This is the first responce from server!  
```

#### 2. Status code 200.

Choose `Status code: Code is 200` snippet
```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Check that the correct string comes in body.

```js
pm.test("EP_2_1. Your test body", function () {
    pm.response.to.have.body('This is the first responce from server!');
});
```

***

### Method `POST`,  URL `http://162.55.220.72:5005/user_info_3`

#### 1. Submit a request.

Response
```
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

Choose `Status code: Code is 200` snippet
```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

#### 3. Parse response body into json.

```js
let responseData = pm.response.json();  
console.log('Response data:', responseData);
```

#### 4. Parse request.
```js
let requestData = pm.request.url.query.toObject();
console.log('Request data:', requestData)
```
