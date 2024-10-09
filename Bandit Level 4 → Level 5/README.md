# Bandit Level 4 → Level 5

## Level Goal
The password for the next level is stored in the only human-readable file in the `inhere` directory.

## Commands You May Need
- `ls`: List directory contents.
- `file`: Determine the type of each file.
- `cat`: Display the contents of a file.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit5@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
   ```


2. **Navigate to the `inhere` Directory**:
   Once logged in, navigate to the `inhere` directory:

   ```
   cd inhere
   ```

3. **Identify the Human-Readable File**:
   Use the `file` command to identify the human-readable file. Since some filenames start with a dash, use the following command to properly handle the filenames:

   ```
   for file in ./-*; do file "$file"; done
   ```

   This will list the type of each file. Look for a file labeled as "ASCII text" or "human-readable."

4. **Read the File**:
   Once you find the human-readable file (e.g., `./-file07`), use the `cat` command to display its contents and get the password for the next level:

   ```
   cat ./-file07
   ```

5. **Password for Level 5**:
   The file contains the password for **Level 5**:
   
   ```
   2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
   ```
