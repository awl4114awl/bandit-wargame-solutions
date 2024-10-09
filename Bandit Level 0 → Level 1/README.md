# Bandit Level 0 → Level 1

## Level Goal
The password for the next level is stored in a file called `readme` located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Commands You May Need
- `ls` : List directory contents.
- `cd` : Change directory.
- `cat` : Display the contents of a file.
- `file` : Determine file type.
- `du` : Estimate file space usage.
- `find` : Search for files.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using SSH. Use the default `bandit0` credentials:
   
   ```bash
   ssh bandit1@bandit.labs.overthewire.org -p 2220
   ```

2. **List the Files in the Home Directory**:
   After logging in, use the `ls` command to list the files in the home directory:
   
   ```bash
   ls
   ```

   You should see a file named `readme`.

3. **Read the Password in the `readme` File**:
   Use the `cat` command to display the contents of the `readme` file, which contains the password for **Level 2**:
   
   ```bash
   cat readme
   ```

   The output will be the password for **Level 2**.

4. **Save the Password**:
   It is important to save the password, as you will need it to access **Bandit Level 1**. It's a good idea to create a local text file for your notes and passwords.

5. **Password for Level 2:**
   ```
   boJ9jbbUNNfktd78OOpsqOltutMc3MY1
   ```
