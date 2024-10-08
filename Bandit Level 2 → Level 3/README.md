# Bandit Level 2 → Level 3

## Level Goal
The password for the next level is stored in a file called `spaces in this filename` located in the home directory. You need to retrieve the password from this file to proceed to Bandit Level 4.

## Commands You May Need
- `ls`: List directory contents.
- `cat`: Display the contents of a file.
- Quoting or escaping filenames with spaces.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit3@bandit.labs.overthewire.org -p 2220
   ```
   - **Password**: The password retrieved from **Level 3**.

2. **List the Files in the Home Directory**:
   Once logged in, use `ls` to list the files in the home directory:

   ```
   ls
   ```

   You should see the file named `spaces in this filename`.

3. **Read the Contents of the File**:
   Since the file name contains spaces, you must either escape the spaces or use quotes. Use one of the following methods to retrieve the password:

   - Using quotes:
     ```
     cat "spaces in this filename"
     ```

   - Escaping spaces:
     ```
     cat spaces\ in\ this\ filename
     ```

4. **Password for Level 4**:
   The file contains the password for **Level 4**: 
   
   ```
   MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
   ```
