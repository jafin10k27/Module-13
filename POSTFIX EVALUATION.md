# Exp.No:34  
## PREFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction.

---

### ALGORITHM

1. **Start the program.**
2. Define a set of valid operators: `*, -, +, %, /, **`.
3. Initialize an empty stack.
4. Traverse the prefix expression from **right to left**:
   - If the character is a **digit**, convert it to an integer and push it onto the stack.
   - If the character is an **operator**, pop two elements from the stack.
     - Apply the operator on the two popped operands.
     - Push the result back onto the stack.
   - If an invalid character is encountered, raise an error.
5. After traversal, the stack should contain only **one element**.
6. Return the **single element** as the evaluation result.
7. **End the program.**

---

### PROGRAM

```python
OPERATORS=set(['*','-','+','%','/','**']) 

def evaluate(expression):
	
	stack = []


	for c in expression[::-1]:

		
		if c not in OPERATORS:
			stack.append(int(c))

		else:
			
			
			o1 = stack.pop()
			o2 = stack.pop()

			if c == '+':
				stack.append(o1 + o2)

			elif c == '-':
				stack.append(o1 - o2)

			elif c == '*':
				stack.append(o1 * o2)

			
	return stack.pop()




test_expression = input()
print("Prefix Expression :",test_expression)
print("Evaluation result :",evaluate(test_expression))


```


### OUTPUT
<img width="762" height="220" alt="image" src="https://github.com/user-attachments/assets/e92f36d9-4a65-4503-9488-8e025f2a9508" />

### RESULT

Thus the python program for to evaluate a user-given Prefix expression using a stack. The expression must contain operators such as Multiplication, Addition, and Subtraction has been implemented and executed successfully.





### RESULT# Exp.No:33  
## POSTFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept.

---

### ALGORITHM

1. **Start the program.**
2. Define a set named `OPERATORS` containing all the valid operators: `*, +, **, -, /, %`.
3. Define a function `evaluate_postfix(exp)` to evaluate the postfix expression:
   - Inside the function, create an empty list called `stack` to store operands and intermediate results.
4. Loop through each item in the given postfix expression:
   - If the current item is **not in OPERATORS**, it is an operand, so append it to the stack.
   - If the current item is an **operator**:
     - Pop the top two elements from the stack (first pop is `a`, second pop is `b`).
     - Perform the operation `b <operator> a` depending on the current operator.
     - Store the result in a variable called `result`.
     - Append the result back to the stack.
5. After the loop ends, return the first element of the stack as the final evaluation result.
6. Take a postfix expression as input from the user.
7. Print the postfix expression.
8. Call the function `evaluate_postfix()` with the input and print the result.
9. **End the program.**

---

### PROGRAM

```python
OPERATORS=set(['*','-','+','%','/','**']) 


def evaluate_postfix(expression):
    stack=[] 
    for i in expression:
        if i not in OPERATORS:
            stack.append(i)  
        
        else:
            a=stack.pop()  
            b=stack.pop()
        
            if i=='+':
                res=int(b)+int(a)  
            elif i=='-':
                res=int(b)-int(a)    
            elif i=='*':
                res=int(b)*int(a)
            elif i=='%':
                res=int(b)%int(a) 
            elif i=='/':
                res=int(b)/int(a)
            elif i=='**':
                res=int(b)**int(a)
    
            stack.append(res) 
    return stack[0]

expression =input()
print('postfix expression: ',expression)
print('Evaluation result: ',evaluate_postfix(expression))


```

### OUTPUT
<img width="721" height="168" alt="image" src="https://github.com/user-attachments/assets/dbf668fe-1c30-408e-bb53-1aba037e3d42" />



### RESULT
Thus the python program for to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept has been implemented and executed successfully.# Exp.No:33  
## POSTFIX EVALUATION

---

### AIM  
To write a Python program to evaluate a user-given Postfix expression that contains Multiplication and Addition operators using the stack concept.

---

### ALGORITHM

1. **Start the program.**
2. Define a set named `OPERATORS` containing all the valid operators: `*, +, **, -, /, %`.
3. Define a function `evaluate_postfix(exp)` to evaluate the postfix expression:
   - Inside the function, create an empty list called `stack` to store operands and intermediate results.
4. Loop through each item in the given postfix expression:
   - If the current item is **not in OPERATORS**, it is an operand, so append it to the stack.
   - If the current item is an **operator**:
     - Pop the top two elements from the stack (first pop is `a`, second pop is `b`).
     - Perform the operation `b <operator> a` depending on the current operator.
     - Store the result in a variable called `result`.
     - Append the result back to the stack.
5. After the loop ends, return the first element of the stack as the final evaluation result.
6. Take a postfix expression as input from the user.
7. Print the postfix expression.
8. Call the function `evaluate_postfix()` with the input and print the result.
9. **End the program.**

---

### PROGRAM

```


```

### OUTPUT


### RESULT

