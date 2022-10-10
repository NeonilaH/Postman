## HW_2 Postman

### http://162.55.220.72:5005/first

#### 1. Submit a request.

Response
```
This is the first responce from server!  
```

#### 2. Status code 200

Choose `Status code: Code is 200` snippet
```
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
