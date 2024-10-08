# Bandit Level 7 → Level 8

## Level Goal
The password for the next level is stored in a file named `data.txt` next to the word "millionth."

## Solution Steps

1. **List Files in the Directory**:
   First, list the files in the current directory to locate `data.txt`:

   ```
   ls
   ```

2. **Search for the Word "millionth"**:
   Use the `grep` command to find the line in `data.txt` that contains the word "millionth" and the corresponding password:

   ```
   grep "millionth" data.txt
   ```

3. **Password for Level 8**:
   ```
   dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
   ```
