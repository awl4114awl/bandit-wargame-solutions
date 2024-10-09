# Bandit Level 10 → Level 11

## Level Goal
The password for the next level is stored in the file `data.txt`, which contains base64 encoded data.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit11@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
   ```

2. **List Files in the Directory**:
   First, list the files in the current directory to ensure `data.txt` is present:

   ```
   ls
   ```

3. **Decode the Base64 Encoded Data**:
   Use the `base64` command with the `-d` option to decode the contents of `data.txt`:

   ```
   base64 -d data.txt
   ```

4. **Password for Level 11**:
   ```
   dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
   ```

## Helpful Reading Material
- [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)
