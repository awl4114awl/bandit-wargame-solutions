# Bandit Level 3 → Level 4

## Level Goal
The password for the next level is stored in a hidden file in the `inhere` directory.

## Commands You May Need
- `ls`: List directory contents.
- `ls -a`: List all files, including hidden files.
- `cat`: Display the contents of a file.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit4@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
   ```

2. **Navigate to the `inhere` Directory**:
   Once logged in, navigate to the `inhere` directory:

   ```
   cd inhere
   ```

3. **List Hidden Files**:
   Since the file is hidden, you will need to use the `-a` option with the `ls` command to display all files, including hidden ones:

   ```
   ls -a
   ```

   You should see a file named `...Hiding-From-You`.

4. **Read the Hidden File**:
   Use the `cat` command to display the contents of the hidden file:

   ```
   cat ...Hiding-From-You
   ```

5. **Password for Level 4**:
   ```
   2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
   ```
