# express-node-refactoring
#### 1. What do you think is wrong with the code, if anything?
Ans: Please refer line 29 and 32

#### 2. Can you see any potential problems that could lead to exceptions?
Ans: Request made by superagent doesnt check the error response first. In case user is not authorized, invitation response might through an exception while extracting
invitaionId and authId within response body.  
With re-factored code, the call is moved inside try catch block so any error in request will go into catch block and
can be handled gracefully. 

#### 3. How would you refactor this code to:
Ans : Please refer refactored.js file. 
Note: There is always a scope of further re-factoring by spliting the db methods in seperate files and making them re-usable. 


#### 4. How might you use the latest JavaScript features to refactor the code?
Ans: Please refer refactored.js file wherein I have tried to use latest JS features like async-await and object destructuring.  
