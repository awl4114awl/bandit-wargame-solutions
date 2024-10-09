### Bandit Level 1 → Level 2

---

### Objective:
The password for the next level is stored in a file called - located in the home directory

---

### Steps:

1. **SSH into the Bandit Server** (using the password obtained from Level 0):

    ```
    ssh bandit2@bandit.labs.overthewire.org -p 2220
    ```
    - **Password**: The password obtained from **Level 1** (`boJ9jbbUNNfktd78OOpsqOltutMc3MY1`)

2. **Locate the File `-`**:
    The password is stored in a file named `-`. Since `-` can be mistaken for a command option, you need to specify the file’s path explicitly when using commands like `cat`.

3. **Read the File**:
    Use `cat` with the `./` prefix to specify that `-` is a filename, not an option:

    ```
    cat ./-
    ```

4. **Password for Level 2**:
    ```
    263JGJPfgU6LtdEvgfWU1XP5yac29mFx
    ```

 

