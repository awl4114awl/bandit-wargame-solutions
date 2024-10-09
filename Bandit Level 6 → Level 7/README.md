# Bandit Level 6 → Level 7

## Level Goal
The password for the next level is stored somewhere on the server and has all of the following properties:
- It is owned by the user `bandit7`.
- It is owned by the group `bandit6`.
- It is 33 bytes in size.

## Commands You May Need
- `find`: Search for files based on ownership and size.
- `cat`: Display the contents of a file.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit7@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
   ```
   
2. **Search for the File**:
   Use the `find` command to locate the file that matches the specified properties:

   ```
   find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
   ```

   - `/`: Search the entire filesystem.
   - `-user bandit7`: File is owned by the user `bandit7`.
   - `-group bandit6`: File is owned by the group `bandit6`.
   - `-size 33c`: File size is exactly 33 bytes.
   - `2>/dev/null`: Suppress permission errors.

3. **Read the File**:
   Once the file is found (`/var/lib/dpkg/info/bandit7.password`), use the `cat` command to read its contents and retrieve the password:

   ```
   cat /var/lib/dpkg/info/bandit7.password
   ```

4. **Password for Level 7**:
   The file contains the password for **Level 7**:
   
   ```
   morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
   ```
