# Bandit Level 14 → Level 15

## Level Goal
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit15@bandit.labs.overthewire.org -p 2220
   ```
   ```
   pasasword: MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
   ```
   - **Password**: The password retrieved from Level 14.

2. **Submit the Password to Port 30000**:
   Use the `nc` (netcat) command to connect to port 30000 and submit the current password:

   ```
   echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc localhost 30000
   ```

3. **Password for Level 15**:
   ```
   8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
   ```
