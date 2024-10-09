# Bandit Level 12 → Level 13

## Level Goal
The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed.

## Solution Steps

1. **Connect to the Bandit Server**:
   Open a terminal and connect to the Bandit server using the following SSH command:
   
   ```
   ssh bandit13@bandit.labs.overthewire.org -p 2220
   ```
   ```
   password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
   ```

2. **Create a Working Directory**:
   To make the process easier, create a working directory in `/tmp`:
   
   ```
   mkdir /tmp/bandit12_extraction
   cd /tmp/bandit12_extraction
   ```

3. **Convert Hexdump to Binary**:
   Use the `xxd` command to reverse the hexdump and save it as a binary file:

   ```
   xxd -r /path/to/data.txt > data.bin
   ```

4. **Identify and Decompress the File**:
   Check the file type and decompress it as needed. Repeat these steps until you reach the final text file:

   - **Check file type**:
     ```
     file data.bin
     ```

   - **For gzip files**:
     ```bash
     mv data.bin data.gz
     gzip -d data.gz
     ```

   - **For bzip2 files**:
     ```
     mv data.bin data.bz2
     bzip2 -d data.bz2
     ```

   - **For tar archives**:
     ```
     tar -xf data.bin
     ```

   - **Repeat the process**: After each extraction, check the file type again and continue extracting until you reach a text file.

5. **Read the Final Text File**:
   When you reach the ASCII text file, use `cat` to read the contents and retrieve the password:

   ```
   cat data8
   ```

6. **Password for Level 13**:
   ```
   FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
   ```

## Helpful Reading Material
- [Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)
