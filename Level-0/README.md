### Bandit Level 0 Objective:
The goal of **Level 0** is to connect to the Bandit game server using SSH and retrieve the password for **Level 1**.

### Steps:

1. **SSH into the Bandit Server**:
   You need to use the SSH protocol to connect to the Bandit server. The server runs on a non-default SSH port (`2220`), so the command to connect looks like this:

   ```bash
   ssh bandit0@bandit.labs.overthewire.org -p 2220
   ```

   - **Username**: `bandit0`
   - **Password**: `bandit0` (This is the initial password)
   - **Port**: `2220`

2. **Find the Password**:
   Once you're logged in, you need to find a file named `readme`. You can use the following commands:
   
   - To list files in the directory:
   
     ```bash
     ls
     ```

   - To read the contents of the `readme` file (which contains the password for the next level):

     ```bash
     cat readme
     ```

3. **Password for Level 1**:
   The file `readme` will contain the password for **Level 1**. After reading it, you can use it to log into the next level.

