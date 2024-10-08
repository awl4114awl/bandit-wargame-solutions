# Bandit Level 13 → Level 14

## Level Goal
The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user `bandit14`. You need to use a private SSH key to log in as bandit14 to retrieve the password.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit13@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
   ```

2. **Use the Private Key to Log in as Bandit14**:
   To retrieve the password, use the provided private SSH key to log in as bandit14:

   ```
   ssh -i sshkey.private bandit14@localhost -p 2220 cat /etc/bandit_pass/bandit14
   ```

   - `-i sshkey.private`: Use the private SSH key for authentication.
   - `bandit14@localhost`: Connect to the localhost as user `bandit14`.

3. **Password for Level 14**:
   ```
   MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
   ```
