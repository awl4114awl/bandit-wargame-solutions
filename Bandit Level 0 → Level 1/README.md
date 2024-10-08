# Bandit Level 0 → Level 1

## Level Goal
The password for the next level (Bandit Level 1) is stored in a file called `readme` located in the home directory. Use this password to log into Bandit1 using SSH on port 2220. 

Once you find a password for a level, use SSH to log into that level and continue the game. Always save the passwords, as they are not saved automatically, and they may change periodically.

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
   ssh bandit0@bandit.labs.overthewire.org -p 2220
   ```

   - **Username**: `bandit0`
   - **Password**: `bandit0`
   - **Port**: `2220`

2. **List the Files in the Home Directory**:
   After logging in, use the `ls` command to list the files in the home directory:
   
   ```bash
   ls
   ```

   You should see a file named `readme`.

3. **Read the Password in the `readme` File**:
   Use the `cat` command to display the contents of the `readme` file, which contains the password for **Level 1**:
   
   ```bash
   cat readme
   ```

   The output will be the password for **Level 1**.

4. **Save the Password**:
   It is important to save the password, as you will need it to access **Bandit Level 1**. It's a good idea to create a local text file for your notes and passwords.

## Password for Level 1
```
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```

## Notes
- This level introduces basic navigation commands in Linux, such as `ls` and `cat`, which will be used throughout the game.
- Remember to keep a record of all passwords and detailed notes as you progress through the levels.
