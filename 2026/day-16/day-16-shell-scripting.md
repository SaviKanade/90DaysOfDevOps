Challenge Tasks

Task 1: Your First Script

1. Create a file hello.sh
2. Add the shebang line #!/bin/bash at the top
3. Print Hello, DevOps! using echo
4. Make it executable and run it
chmod +x hello.sh
./hello.sh
<img width="482" height="163" alt="Screenshot 2026-02-13 at 5 14 46 PM" src="https://github.com/user-attachments/assets/18010b26-e767-4342-a13b-9d933d620f84" />

Document: What happens if you remove the shebang line?
-> Nothing happens. This line tells the server of a shell used by the script.


Task 2: Variables

1. Create variables.sh with:
    * A variable for your NAME
    * A variable for your ROLE (e.g., "DevOps Engineer")
    * Print: Hello, I am <NAME> and I am a <ROLE>
<img width="458" height="207" alt="Screenshot 2026-02-13 at 5 18 42 PM" src="https://github.com/user-attachments/assets/cc5dd25d-64b2-4590-bb66-1d719fed286e" />

2. Try using single quotes vs double quotes — what's the difference?
-> There is no difference while printing but as per my understanding those are used in many different ways.


Task 3: User Input with read

1. Create greet.sh that:
    * Asks the user for their name using read
    * Asks for their favourite tool
    * Prints: Hello <name>, your favourite tool is <tool>
<img width="520" height="250" alt="Screenshot 2026-02-13 at 5 24 06 PM" src="https://github.com/user-attachments/assets/ec63c2d2-ffd4-4d21-9225-30a86b5a67b9" />


Task 4: If-Else Conditions

1. Create check_number.sh that:
    * Takes a number using read
    * Prints whether it is positive, negative, or zero
<img width="543" height="399" alt="Screenshot 2026-02-13 at 6 31 38 PM" src="https://github.com/user-attachments/assets/da7c2b02-8a77-4f3e-9935-9627a64741d2" />

2. Create file_check.sh that:
    * Asks for a filename
    * Checks if the file exists using -f
    * Prints appropriate message
<img width="565" height="332" alt="Screenshot 2026-02-13 at 5 37 59 PM" src="https://github.com/user-attachments/assets/b00ed710-ce67-4658-9158-3107777f6a01" />


Task 5: Combine It All

Create server_check.sh that:
1. Stores a service name in a variable (e.g., nginx, sshd)
2. Asks the user: "Do you want to check the status? (y/n)"
3. If y — runs systemctl status <service> and prints whether it's active or not
4. If n — prints "Skipped."
<img width="1241" height="596" alt="Screenshot 2026-02-13 at 6 10 19 PM" src="https://github.com/user-attachments/assets/657fb53f-edc9-44d8-9368-211fa938200e" />



* What you learned (3 key points)
1. Learned about very detailed smaller things. For eg. we have to give space in IF condition.
2. The working of operators is quite different in shell scripting. Like, in python,C we use == operator for string/integer comparison but here its different for numeric & string. for string it use only '=' and for numeric value its '==' or '-eq'.
3. Learned about syntaxes which I wasn't even aware of & the structure of shell scripting. (if/for/operators/print) 


1. Add your scripts and day-16-shell-scripting.md to 2026/day-16/
2. Commit and push to your fork
