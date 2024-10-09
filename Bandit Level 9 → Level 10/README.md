# Bandit Level 9 → Level 10

## Level Goal
The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several `=` characters.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit10@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
   ```

2. **List Files in the Directory**:
   First, list the files in the current directory to ensure `data.txt` is present:

   ```
   ls
   ```

3. **Extract Human-Readable Strings**:
   Use the `strings` command to extract the human-readable strings from `data.txt` and filter for lines that contain multiple `=` characters:

   ```
   strings data.txt | grep "===="
   ```

4. **Password for Level 10**:
   ```
   FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
   ```
