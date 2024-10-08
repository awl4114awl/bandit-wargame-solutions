# Bandit Level 11 → Level 12

## Level Goal
The password for the next level is stored in the file `data.txt`, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit11@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
   ```

2. **List Files in the Directory**:
   First, list the files in the current directory to ensure `data.txt` is present:

   ```
   ls
   ```

3. **Decode the ROT13 Encoded Data**:
   Use the `tr` command to decode the ROT13-encoded contents of `data.txt`:

   ```
   cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
   ```

4. **Password for Level 12**:
   ```
   7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
   ```

## Helpful Reading Material
- [Rot13 on Wikipedia](https://en.wikipedia.org/wiki/ROT13)
