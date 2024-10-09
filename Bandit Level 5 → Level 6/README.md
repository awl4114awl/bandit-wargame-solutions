# Bandit Level 5 → Level 6

## Level Goal
The password for the next level is stored in a file somewhere under the `inhere` directory and has all of the following properties:

```
human-readable
1033 bytes in size
not executable
```

## Commands You May Need
- `find`: Search for files with specific properties.
- `cat`: Display the contents of a file.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit6@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
   ```

2. **Navigate to the `inhere` Directory**:
   Once logged in, navigate to the `inhere` directory:

   ```
   cd inhere
   ```

3. **Find the Correct File**:
   Use the `find` command to search for the file that meets the specified criteria:

   ```
   find . -type f -size 1033c ! -executable
   ```

   - `.`: Search in the current directory and all subdirectories.
   - `-type f`: Only look for regular files.
   - `-size 1033c`: File size of exactly 1033 bytes.
   - `! -executable`: Exclude executable files.

4. **Read the File**:
   Once you find the correct file, use the `cat` command to display its content and retrieve the password:

   ```
   cat ./maybehere07/.file2
   ```

5. **Password for Level 6**:
   ```
   HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
   ```
