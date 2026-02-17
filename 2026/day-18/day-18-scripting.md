Challenge Tasks

**Task 1: Basic Functions**
<img width="746" height="432" alt="Screenshot 2026-02-17 at 4 29 56 PM" src="https://github.com/user-attachments/assets/414888f5-d6a0-47cf-874f-5ef1f35b6ad6" />


**Task 2: Functions with Return Values**
<img width="704" height="578" alt="Screenshot 2026-02-17 at 4 33 44 PM" src="https://github.com/user-attachments/assets/b3197cd0-2aa4-41f1-a06f-d8cf80d682fa" />


**Task 3: Strict Mode — set -euo pipefail**
Create strict_demo.sh with set -euo pipefail at the top
Try using an undefined variable — what happens with set -u?
Try a command that fails — what happens with set -e?
Try a piped command where one part fails — what happens with set -o pipefail?
Document: What does each flag do?

set -e → Breaks the script
set -u → Undefined variable
set -o pipefail → 1st pipeline fails it exits the code
<img width="701" height="474" alt="Screenshot 2026-02-17 at 4 52 21 PM" src="https://github.com/user-attachments/assets/1a458bf3-f5ed-4dd0-9721-58d58eccbc08" />
<img width="812" height="302" alt="Screenshot 2026-02-17 at 4 50 10 PM" src="https://github.com/user-attachments/assets/23fff890-1c86-4386-9e97-2607bff5e9ec" />


**Task 4: Local Variables**
Create local_demo.sh with:
A function that uses local keyword for variables
Show that local variables don't leak outside the function
Compare with a function that uses regular variables
<img width="670" height="472" alt="Screenshot 2026-02-17 at 5 04 38 PM" src="https://github.com/user-attachments/assets/e91eff3f-959d-477d-9ba1-34fa36acda8d" />

Comment :
Basically, a variable which is defined locally & inside a function cannot be accessed by globally by any functions.
And a regular variable can be accessbed globally by any function. 



**Task 5: Build a Script — System Info Reporter**
Create system_info.sh that uses functions for everything:

A function to print hostname and OS info
A function to print uptime
A function to print disk usage (top 5 by size)
A function to print memory usage
A function to print top 5 CPU-consuming processes
A main function that calls all of the above with section headers
Use set -euo pipefail at the top

<img width="737" height="587" alt="Screenshot 2026-02-17 at 5 23 56 PM" src="https://github.com/user-attachments/assets/171bb107-e91d-4054-bd1c-10e4ae3543f4" />
<img width="615" height="631" alt="Screenshot 2026-02-17 at 5 24 21 PM" src="https://github.com/user-attachments/assets/1f1caf5d-2b9b-4d4f-a710-44dc11895b63" />



**set -euo pipefail**
set -e → Breaks the script
set -u → Undefined variable
set -o pipefail → 1st pipeline fails it exits the code


**What you learned (3 key points)**
1. Working with functions.
2. How we can use commands in functions.
3. Usage & work of awk command.
