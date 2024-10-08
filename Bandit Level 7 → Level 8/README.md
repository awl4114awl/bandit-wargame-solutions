# Bandit Level 7 → Level 8

## Level Goal
The password for the next level is stored in a file named `data.txt` next to the word "millionth."

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit7@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
   ```


2. **List Files in the Directory**:
   First, list the files in the current directory to locate `data.txt`:

   ```
   ls
   ```

3. **Search for the Word "millionth"**:
   Use the `grep` command to find the line in `data.txt` that contains the word "millionth" and the corresponding password:

   ```
   grep "millionth" data.txt
   ```

4. **Password for Level 8**:
   ```
   dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
   ```
