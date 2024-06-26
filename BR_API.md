# Bug Report test challenge API part
#### Type: Bug
#### Severity: High
#### Priority: High
#### Status: To Do
#### Note: All cases begins as from the start, not related one with other

## Precondition:
1. Go to URL: https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login
2. Into Username input type "TestUser389"
3. Into Password input type "^9!jT@y#)SOP"
4. Press "Log In" button


### Case 1:
#### Steps to reproduce:
1. Do Precondition
2. Go to postmans collection "Add Employee"
3. Press "Try/Send"
4. Go back to app
5. Insure that new Employee is created
6. Copy this Employees ID
7. Go to postmans collection "Delete Employee"
8. Paste ID at the end of URL instead of {{id}}
9. Go back to app
10. Look for deleted Employees
11. Repeat steps 7,8
12. Look at status code


#### Expected result: 
Status code will warn that this action is impossible

#### Actual result:
Status code is still 200, and no info that the user has been removed already



### Case 2:
#### Steps to reproduce:
1. Do Precondition
2. Remove all Employees if there are some
3. Go to postmans collection "Update Employee"
4. Press "Try/Send"
5. Go back to app


#### Expected result: 
If theres no Employees cretaed, then noone to update

#### Actual result:
While updating Employee in postman with update collection creates new user. If send request with same data couple of times, then in app will be created more and more Employees, but with new IDs. But in request ID in Body is set to be the same

<img width="1176" alt="Screenshot 2024-06-16 at 13 47 44" src="https://github.com/ioannrio/str/assets/15255256/72d34328-6b84-4a84-98b5-f10bce994e9e">
<img width="1440" alt="Screenshot 2024-06-16 at 13 47 35" src="https://github.com/ioannrio/str/assets/15255256/19f05cf0-5f67-4190-8748-8bbe30c24b63">


### Case 3:
#### Steps to reproduce:
1. Do Precondition
2. Go to postmans collection "Add Employee"
3. Press "Try/Send"
4. Copy id
5. Go back to app
6. Insure that new Employee is created
7. Copy this Employees ID
8. Go to postmans collection "Add Employee"
9. Paste same id in the request body
10. Go back to app
11. Look for Employees


#### Expected result: 
Warning will appear that id has been taken already

#### Actual result:
Now is possible to send request with the same id while adding new Employee. But newly created Employee has new id instead, this brings some confusion



### Case 4:
#### Steps to reproduce:
1. Do Precondition
2. Go to postmans collection "Update Employee"
3. In body add another id (firstName aso)
4. Press "Try/Send"
6. Go back to app
7. Look if new Employee is created


#### Expected result: 
Warning will appear that id (firstName aso) has been taken already

#### Actual result:
Now is possible to send request with the same id (firstName aso) while adding new Employee

<img width="1436" alt="Screenshot 2024-06-16 at 14 29 06" src="https://github.com/ioannrio/str/assets/15255256/98924a5e-7694-4ed2-8829-04aa88832c47">
<img width="1436" alt="Screenshot 2024-06-16 at 14 26 36" src="https://github.com/ioannrio/str/assets/15255256/09ae81d5-a07f-48b1-be8a-66d072ae39e7">

