Challenge Tasks

Task 1: For Loop

1. Create for_loop.sh that:
    * Loops through a list of 5 fruits and prints each one
2. Create count.sh that:
    * Prints numbers 1 to 10 using a for loop
<img width="635" height="581" alt="Screenshot 2026-02-17 at 12 58 46 PM" src="https://github.com/user-attachments/assets/445b16f3-e995-46fa-b95f-87a85afe2f3b" />



Task 2: While Loop

1. Create countdown.sh that:
    * Takes a number from the user
    * Counts down to 0 using a while loop
    * Prints "Done!" at the end
<img width="609" height="373" alt="Screenshot 2026-02-17 at 3 10 55 PM" src="https://github.com/user-attachments/assets/edc46c75-0193-4150-9d22-5907bf159882" />



Task 3: Command-Line Arguments

1. Create greet.sh that:
    * Accepts a name as $1
    * Prints Hello, <name>!
    * If no argument is passed, prints "Usage: ./greet.sh "
<img width="634" height="315" alt="Screenshot 2026-02-17 at 12 59 37 PM" src="https://github.com/user-attachments/assets/790bf671-27cf-42b6-a3a0-39d0841d51d6" />


2. Create args_demo.sh that:
    * Prints total number of arguments ($#)
    * Prints all arguments ($@)
    * Prints the script name ($0)
<img width="614" height="209" alt="Screenshot 2026-02-17 at 1 00 00 PM" src="https://github.com/user-attachments/assets/b3d6b79b-b238-4ae5-9fd5-b6c995bb1632" />



Task 4: Install Packages via Script

1. Create install_packages.sh that:
    * Defines a list of packages: nginx, curl, wget
    * Loops through the list
    * Checks if each package is installed (use dpkg -s or rpm -q)
    * Installs it if missing, skips if already present
    * Prints status for each package
Run as root: sudo -i or sudo su
<img width="638" height="547" alt="Screenshot 2026-02-17 at 4 18 18 PM" src="https://github.com/user-attachments/assets/942dc758-e2d3-4210-b5b4-9f2877eb5ce4" />



Task 5: Error Handling

1. Create safe_script.sh that:
    * Uses set -e at the top (exit on error)
    * Tries to create a directory /tmp/devops-test
    * Tries to navigate into it
    * Creates a file inside
    * Uses || operator to print an error if any step fails
Example:
mkdir /tmp/devops-test || echo "Directory already exists"
Note : With set -e script is breaking.
<img width="1148" height="303" alt="Screenshot 2026-02-17 at 3 42 29 PM" src="https://github.com/user-attachments/assets/1f5cc720-65ac-4122-9dad-b6bf9ca4cf23" />

Note : Without set -e code is running.
<img width="1189" height="309" alt="Screenshot 2026-02-17 at 3 44 31 PM" src="https://github.com/user-attachments/assets/e37741de-b3c7-4125-ae30-57ed7ad48e8b" />



3 key points :
1. Learned about conditional differences used in loops.
2. How to use the proper syntax for each scripting concept.
3. Small details about the syntax but mostly getting confused between "$i" & $i. Like how they are working?
