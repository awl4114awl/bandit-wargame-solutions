# Bandit Level 8 → Level 9

## Level Goal
The password for the next level is stored in the file `data.txt` and is the only line of text that occurs only once.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit9@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
   ```

2. **List Files in the Directory**:
   First, list the files in the current directory to locate `data.txt`:

   ```
   ls
   ```

3. **Find the Unique Line**:
   Use the following command to find the unique line (the line that occurs only once) in `data.txt`:

   ```
   sort data.txt | uniq -u
   ```

4. **Password for Level 9**:
   ```
   4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
   ```
## Helpful Reading Material
[Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)
