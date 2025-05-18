# Using-tools-like-John-the-Ripper-for-password-cracking
## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).

### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:

- **Install the John Ripper**
  ```bash
  sudo apt install john
  ```
- **Create a Password-Protected ZIP File**
   Archive a normal file (secret.txt) into a password-protected ZIP file
   ```bash
   zip --password 123abc secret.txt.zip secret.txt
   ```
 - **Extract the Hash from the ZIP File**
   ```bash
   zip2john secret.txt.zip > zip_hash.txt
   ```
- **Crack the ZIP Password using John**
  ```bash
  john --format=zip zip_hash.txt
  ```
- **Show the Cracked Password**
  ```bash
  john --show zip_hash.txt
  ```

## OUTPUT:
### Create a Password-Protected ZIP File
![image](https://github.com/user-attachments/assets/92fc7fa4-3e0b-440b-9b35-d0fc061fc83d)


### Extract the Hash from the ZIP File
![image](https://github.com/user-attachments/assets/5679584f-760e-46d3-b497-1922fd67a4ff)


![image](https://github.com/user-attachments/assets/ecd5e14a-6d96-47bd-9c84-e721b811680c)


### Crack the ZIP Password using John
![image](https://github.com/user-attachments/assets/f7b5d503-b6e3-46b5-b901-28ace33ed831)


### Show the Cracked Password
![image](https://github.com/user-attachments/assets/b56c611a-5884-4397-821e-d4e2bb420252)


## RESULT:
The password hashes were successfully cracked using John the Ripper.
