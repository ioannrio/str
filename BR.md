# Bug Report test challenge
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
2. Press "Add Employee"
3. Into "First Name:" input type "John"
4. Into "Last Name:" input type "Surf"
5. Into "Dependents:" input type "33"
6. Press "Add" button


#### Expected result: 
Warning should be appeared

#### Actual result:
No warning appears. Employee can not be added if Dependents are higher then INT "33". In descriptions is no information about it. Only in Logs

<img width="1435" alt="Screenshot 2024-06-15 at 12 56 33" src="https://github.com/ioannrio/str/assets/15255256/aac6f081-810a-48a5-87cf-f3c1bcff3a1c">



### Case 2: 
#### Steps to reproduce:
1. Do Precondition
2. Wait for a while until expiration login time ends cuz of inactivity
3. Refresh page

#### Expected result:
User get logged out cuz of inactivity, or nothing happens

#### Actual result:
No user data is available and no "Log out" option is available

<img width="1434" alt="Screenshot 2024-06-15 at 13 09 12" src="https://github.com/ioannrio/str/assets/15255256/4018ecbc-1067-41aa-a81d-b21608be1c78">


### Case 3:
#### Steps to reproduce:
1. Do Precondition
2. Wait for a while until expiration login time ends cuz of inactivity
3. Press "Add Employee"
4. Into "First Name:" input type "John"
5. Into "Last Name:" input type "Surf"
6. Into "Dependents:" input type "1"
7. Press "Add" button

#### Expected result:
Warning should be appeared

#### Actual result:
No warning appears and employee can't be added. In log only info with status code 401

<img width="1435" alt="Screenshot 2024-06-15 at 14 09 16" src="https://github.com/ioannrio/str/assets/15255256/9cc2a954-5515-480a-aebc-7c1e773408d9">

#### Note: Same with edit or delete employee



### Case 4:
#### Steps to reproduce:
1. Do Precondition
2. Set screen view to mobile one

#### Expected result:
Screen is set to be mobile browser friendly

#### Actual result:
For phone and pad is not friendly design

<img width="1434" alt="Screenshot 2024-06-15 at 13 10 05" src="https://github.com/ioannrio/str/assets/15255256/d91ff6dc-4411-4e2e-92da-146ff58c0e7e">



### Case 5:
#### Steps to reproduce:
1. Do Precondition
2. Wait for a while until expiration login time ends cuz of inactivity
3. Press "Add Employee"
4. Into "First Name:" input type "John"
5. Into "Last Name:" input type "Surf"
6. Into "Dependents:" input type "1"
7. Press "Add" button
8. Press Edit icon near to created employee
9. Into "Dependents:" input type "0.7"
10. Press "Update" button


#### Expected result:
Dependents will be 0.7 or warning appears that it's not possible

#### Actual result:
Dependents if is updated to 0.7 is viewed as 0. In network as well

<img width="1436" alt="Screenshot 2024-06-15 at 17 18 34" src="https://github.com/ioannrio/str/assets/15255256/564eb56b-560d-41ed-9f2b-ae62e98f4249">

#### Note: If it is not allowed, theres no info provided. And Warning needs to be added




### Case 6:
#### Steps to reproduce:
1. Do Precondition
2. Wait for a while until expiration login time ends cuz of inactivity
3. Press "Add Employee"
4. Into "First Name:" input type "Ivan"
5. Into "Last Name:" input type "Surf"
6. Into "Dependents:" input type "ioweruwoir"
7. Press "Add" button


#### Expected result:
Warning should be appeared

#### Actual result:
No warning appears and employee can't be added. In network only info with status code 405, and Dependents - null

<img width="1435" alt="Screenshot 2024-06-15 at 17 33 26" src="https://github.com/ioannrio/str/assets/15255256/22038cc9-bbb2-46f6-9654-e469b561ffe0">


### Case 7: 
#### Steps to reproduce:
1. Do Precondition
2. Wait for a while until expiration login time ends cuz of inactivity
3. Refresh page
4. Copy URL
5. Paste in a new tab copied URL

#### Expected result:
User get logged out cuz of inactivity, or nothing happens. After pasting in new tab, then user can loggin again

#### Actual result:
No user data is available and no "Log out" option is available, new tab didn't changed a thing, only 403 Forbidden appears



### Case 8:
#### Steps to reproduce:
1. Do Precondition
2. Wait for a while until expiration login time ends cuz of inactivity
3. Press "Add Employee"
4. Into "First Name:" input type "Kyiv is the capital and most populous city of Ukraine. It is in north-central Ukraine along the Dnieper River. As of 1 January 2022, its population was 2,952,301 making Kyiv the seventh-most populous city in Europe. Kyiv is an important industrial, scientific, educational, and cultural center in Eastern Europe"
5. Into "Last Name:" input type "Kyiv is the capital and most populous city of Ukraine. It is in north-central Ukraine along the Dnieper River. As of 1 January 2022, its population was 2,952,301 making Kyiv the seventh-most populous city in Europe. Kyiv is an important industrial, scientific, educational, and cultural center in Eastern Europe"
6. Into "Dependents:" input type "3"
7. Press "Add" button


#### Expected result:
Warning should be appeared

#### Actual result:
No warning appears and employee can't be added. In network only info with status code 400, and description that max length can be 50 characters



### Case 9:
#### Steps to reproduce:
1. Do Precondition
2. Press "Add Employee"
3. Press "Add" button


#### Expected result:
Warning should be appeared

#### Actual result:
No warning appears and employee can't be added. In network only info with status code 405

<img width="1434" alt="Screenshot 2024-06-15 at 20 39 52" src="https://github.com/ioannrio/str/assets/15255256/6f34ca09-b46a-465d-9cfd-5dc7f49cfc64">


### Case 10:
#### Steps to reproduce:
1. Do Precondition
2. Press "Add Employee"
3. Into "First Name:" input type "John"
4. Into "Last Name:" input type "Surf"
5. Into "Dependents:" input type "-8"
6. Press "Add" button


#### Expected result:
Warning should be appeared

#### Actual result:
No warning appears and employee can't be added. In network only info with status code 400, and description that allowed characteers are from 0 to 32

<img width="1436" alt="Screenshot 2024-06-15 at 20 44 26" src="https://github.com/ioannrio/str/assets/15255256/a1148269-0d3d-4180-b534-242dab2b55c9">
<img width="1440" alt="Screenshot 2024-06-15 at 20 44 16" src="https://github.com/ioannrio/str/assets/15255256/346398cd-f566-49d5-ace9-e9109392e3ff">

#### NOTE: Not obvious from requirements how the "Benefits Cost" anf "Net Pay" are calculated, is needed more info

