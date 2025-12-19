# Bandit Wargame: A Beginner's Guide to Linux Security

## bandit-linux-security-project Level 0 - Level 34


# Bandit Level 0 

### Level Goal:

The goal of this level is to log into the game using **SSH**. You need to connect to the following host:

* **Host**: `bandit.labs.overthewire.org`
* **Port**: `2220`
* **Username**: `bandit0`
* **Password**: `bandit0`

Once logged in, you will find the password for **Level 1** stored in a file called **readme** in the home directory. After finding the password, you can proceed to **Level 1**.

---

### Commands You May Need:

* `ssh` – To log into the server.
* `ls` – To list the contents of the current directory.
* `cat` – To read the contents of a file.

---

### Solution Step by Step:

1. **Log into the Bandit Level 0 via SSH**:
   Use the `ssh` command to connect to the server.

   ```bash
   ssh bandit0@bandit.labs.overthewire.org -p 2220
   ```

   * **Explanation**:

     * `ssh`: This command is used to securely connect to a remote server over the internet.
     * `bandit0@bandit.labs.overthewire.org`: This is the username (`bandit0`) and the host (`bandit.labs.overthewire.org`) you are trying to connect to.
     * `-p 2220`: This flag specifies the port number to connect to. The challenge uses port 2220.

2. **Enter the password** when prompted:

   ```bash
   bandit0
   ```

   * **Explanation**:
     This is the password for the **bandit0** account that you need to input to log in.

3. **List the files in the current directory**:
   After logging in, use the `ls` command to check the contents of the home directory.

   ```bash
   ls
   ```

   * **Explanation**:

     * `ls`: Lists the files and directories in the current directory. In this case, it shows the `readme` file that contains the password for **Level 1**.

4. **Read the contents of the `readme` file**:
   Use the `cat` command to view the contents of the `readme` file.

   ```bash
   cat readme
   ```

   * **Explanation**:

     * `cat`: The `cat` command is used to display the contents of a file. Here, it reveals the password for **Level 1**.

   * **Output**:

     ```
     ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
     ```

   The password for **Level 1** is:

   ```
   ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
   ```

---

### Next Steps:

* Use the password found in the `readme` file to log into **bandit1**:

  ```bash
  ssh bandit1@bandit.labs.overthewire.org -p 2220
  ```
* Enter the password you just found when prompted.

---



# Bandit Level 0 → Level 1

### Level Goal:

The goal of this level is to log into the game using **SSH**. Once logged in, the password for the next level is stored in a file called **`readme`** located in the home directory. After obtaining the password, use it to log into **bandit1**.

---

### Commands You May Need:

* `ssh`: To log into a remote machine via SSH.
* `ls`: To list the contents of a directory.
* `cat`: To read the contents of a file.
* `whoami`: To display the current logged-in username.
* `exit`: To exit the current SSH session.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 1 via SSH**:

First, use the password obtained from **Level 0** to log into **bandit1**.

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects you to the remote server.
  * `bandit1@bandit.labs.overthewire.org`: Specifies the username (`bandit1`) and the host (`bandit.labs.overthewire.org`) to connect to.
  * `-p 2220`: Specifies the port number to connect to.

#### 2. **Enter the password** when prompted:

You will be asked to enter the password that you found in **Level 0**'s `readme` file. Enter the password:

```bash
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```

#### 3. **Check the username**:

After logging in, verify that you are on **bandit1** by running the `whoami` command:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user. You should see `bandit1` confirming you're on the correct account.

* **Expected output**:

  ```
  bandit1
  ```

#### 4. **List the files in the current directory**:

Run the `ls` command to view the files in the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists files and directories in the current directory.
    In this case, it will show a file, which may be an odd name (represented as `-` here).

* **Expected output**:

  ```
  -
  ```

#### 5. **Read the contents of the file**:

Use the `cat` command to display the contents of the file. Notice that the file has a name of `-` (a hyphen), which may be tricky to reference directly. You can use `./-` to access it.

```bash
cat ./-
```

* **Explanation**:

  * `cat`: Reads and displays the contents of a file.
  * `./-`: Refers to the file named `-` in the current directory (the `./` tells the system to look in the current directory).

* **Expected output**:

  ```
  263JGJPfgU6LtdEvgfWU1XP5yac29mFx
  ```

This is the password for **Level 2**.

#### 6. **Exit the SSH session**:

Once you have the password for Level 2, you can exit the SSH session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out of the server.

---

# Bandit Level 1 → Level 2

### Level Goal:

The password for the next level is stored in a file called **`-`** located in the home directory. Once you retrieve the password, you can use it to log into **bandit2**.

---

### Commands You May Need:

* `ls`: To list the contents of the current directory.
* `cd`: To change directories.
* `cat`: To read the contents of a file.
* `file`: To determine the type of a file.
* `du`: To check disk usage of files and directories.
* `find`: To search for files or directories.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 1**:

First, log into **bandit1** using SSH (assuming you already have the password from Level 0).

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server via SSH.
  * `bandit1@bandit.labs.overthewire.org`: Specifies the username (`bandit1`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **List the files in the current directory**:

Use the `ls` command to list files in the home directory.

```bash
ls
```

* **Explanation**:

  * `ls`: Lists files and directories in the current directory.
    This will show the file **`-`** (a hyphen), which contains the password for **Level 2**.

* **Expected output**:

  ```
  -
  ```

#### 3. **Read the contents of the `-` file**:

The file is named `-`, which can be confusing since `-` is used as an option for many commands. You will need to use `./-` to specify the file.

```bash
cat ./-
```

* **Explanation**:

  * `cat`: Reads the contents of a file.
  * `./-`: Refers to the file named `-` in the current directory (using `./` tells the system to refer to the file in the current directory, avoiding issues with `-` being interpreted as an option).

* **Expected output**:

  ```
  5f2d0d25f76f1533b081c2b1107f2f74
  ```

This is the password for **Level 2**.

#### 4. **Log into Bandit Level 2**:

Now that you have the password, you can log into **bandit2** using the following SSH command:

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Connects to the remote server.
  * `bandit2@bandit.labs.overthewire.org`: Specifies the username (`bandit2`) and host.
  * `-p 2220`: Specifies the port number.

Enter the password you found in **Level 1** when prompted.

#### 5. **Check the username**:

You can verify you're logged in as **bandit2** by running the `whoami` command:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in username.

* **Expected output**:

  ```
  bandit2
  ```

#### 6. **List the files in the current directory**:

Run `ls` again to see the files in the home directory of **bandit2**.

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory. The file you need to access has a name that contains spaces, so you'll need to handle that properly.

* **Expected output**:

  ```
  --spaces in this filename--
  ```

#### 7. **Read the contents of the file with spaces**:

The file's name contains spaces, so you'll need to correctly handle it. You can use quotes to reference the file with spaces in its name:

```bash
cat -- "--spaces in this filename--"
```

* **Explanation**:

  * `cat`: Displays the contents of a file.
  * `-- "--spaces in this filename--"`: The `--` is used to end the options for the `cat` command. The filename with spaces is enclosed in quotes to ensure it's read correctly.

* **Expected output**:

  ```
  MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
  ```

This is the password for **Level 3**.

#### 8. **Exit the SSH session**:

Once you have the password for **Level 3**, you can exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Handling Filenames with Spaces**: Filenames containing spaces need to be quoted or escaped properly. In this case, we use `-- "--spaces in this filename--"` to access the file.
* **Password Management**: Always save the passwords you find in a secure place, as they won’t be saved automatically.

---


# Bandit Level 2 → Level 3

### Level Goal:

The password for the next level is stored in a file called **`--spaces in this filename--`** located in the **home directory**. Once you retrieve the password, you can use it to log into **bandit3**.

---

### Commands You May Need:

* `ls`: To list the contents of the current directory.
* `cd`: To change directories.
* `cat`: To read the contents of a file.
* `file`: To determine the type of a file.
* `du`: To check disk usage of files and directories.
* `find`: To search for files or directories.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 2**:

First, log into **bandit2** using SSH (you should already have the password from Level 1).

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit2@bandit.labs.overthewire.org`: Specifies the username (`bandit2`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password that you found in **Level 2**'s `cat ./-` command.

```bash
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```

#### 3. **Verify the username**:

You can check the current logged-in user by running:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user.

* **Expected output**:

  ```
  bandit3
  ```

#### 4. **List the files in the current directory**:

Run the `ls` command to check the files in the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.
    In this case, you should see a folder called **`inhere`**.

* **Expected output**:

  ```
  inhere
  ```

#### 5. **Navigate into the `inhere` directory**:

Change into the **`inhere`** directory to see what files are inside:

```bash
cd inhere/
```

* **Explanation**:

  * `cd inhere/`: Changes the directory to **`inhere`**.

#### 6. **List the files in the `inhere` directory**:

Run the `ls` command again to list the files in the **`inhere`** directory.

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.
    You might not see anything initially.

* **Expected output**:

  ```
  (empty)
  ```

#### 7. **List the files with detailed information**:

Use the `ls -la` command to get detailed information about the files in the directory:

```bash
ls -la
```

* **Explanation**:

  * `ls -la`: Lists all files, including hidden files, along with detailed information (permissions, owner, etc.).

* **Expected output**:

  ```
  total 12
  drwxr-xr-x 2 root    root    4096 Oct 14 09:26 .
  drwxr-xr-x 3 root    root    4096 Oct 14 09:26 ..
  -rw-r----- 1 bandit4 bandit3   33 Oct 14 09:26 ...Hiding-From-You
  ```

Here you see a file named **`...Hiding-From-You`**. This is the file that contains the password for **Level 3**.

#### 8. **Read the contents of the file**:

To read the contents of the file with a name that contains spaces and special characters, use the `cat` command with `--` to properly handle the filename.

```bash
cat -- "...Hiding-From-You"
```

* **Explanation**:

  * `cat`: Reads and displays the contents of a file.
  * `-- "...Hiding-From-You"`: The `--` signals the end of options for the `cat` command. The filename with spaces is enclosed in quotes to ensure it’s interpreted correctly.

* **Expected output**:

  ```
  2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
  ```

This is the password for **Level 3**.

#### 9. **Exit the SSH session**:

Once you have the password for **Level 3**, you can exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session.

---

### Notes:

* **Handling Filenames with Special Characters**: Filenames like **`...Hiding-From-You`** that contain spaces and other special characters need to be referenced correctly using quotes or `--`.
* **Password Management**: Always save the passwords you find for future use as they are not stored automatically.


# Bandit Level 3 → Level 4

### Level Goal:

The password for the next level is stored in a **hidden file** within the **inhere** directory. Your task is to locate and read the file that contains the password for **Level 4**.

---

### Commands You May Need:

* `ls`: To list the contents of the current directory.
* `cd`: To change directories.
* `cat`: To display the contents of a file.
* `file`: To determine the type of a file.
* `du`: To check disk usage of files and directories.
* `find`: To search for files or directories.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 3**:

Use SSH to log into **bandit3** using the password you retrieved in **Level 2**.

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit3@bandit.labs.overthewire.org`: Specifies the username (`bandit3`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 3**.

```bash
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```

#### 3. **Verify the username**:

Check if you are logged in as **bandit4**:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the currently logged-in username.

* **Expected output**:

  ```
  bandit4
  ```

#### 4. **List the files in the current directory**:

Use the `ls` command to view the files in the home directory of **bandit4**:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files and directories in the current directory.
    In this case, you should see the **`inhere`** directory.

* **Expected output**:

  ```
  inhere
  ```

#### 5. **Change into the `inhere` directory**:

Navigate into the **`inhere`** directory where the hidden file is located:

```bash
cd inhere/
```

* **Explanation**:

  * `cd inhere/`: Changes the current directory to **`inhere`**.

#### 6. **List the files in the `inhere` directory**:

Use the `ls` command again to view the files inside the **`inhere`** directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the **`inhere`** directory.
    The files are named **`-file00`** to **`-file09`**.

* **Expected output**:

  ```
  -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
  ```

#### 7. **Read the contents of a file with a special name**:

Use the `cat` command to read the contents of one of the files. In this case, we'll read **`-file07`**:

```bash
cat -- -file07
```

* **Explanation**:

  * `cat`: Displays the contents of a file.
  * `--`: Signals the end of options for the `cat` command. This is used because `-file07` starts with a dash (`-`), which can be interpreted as an option.
  * `-file07`: The filename of the file to read.

* **Expected output**:

  ```
  4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
  ```

This is the password for **Level 4**.

#### 8. **Exit the SSH session**:

Once you have the password for **Level 4**, you can exit the SSH session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Files with Special Characters**: When dealing with files starting with a dash (`-`), always use `--` to prevent commands from interpreting them as options. This is particularly useful with commands like `cat`.
* **Password Management**: Make sure to save the passwords you find, as they will not be stored automatically.


# Bandit Level 4 → Level 5

### Level Goal:

The password for the next level is stored in the **only human-readable file** in the **inhere** directory. If your terminal is messed up, you can use the `reset` command to clean the terminal screen.

---

### Commands You May Need:

* `ls`: To list the contents of the current directory.
* `cd`: To change directories.
* `cat`: To display the contents of a file.
* `find`: To search for files or directories.
* `reset`: To reset the terminal if it's not displaying correctly.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 4**:

Use SSH to log into **bandit4** (you should already have the password from **Level 3**).

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit4@bandit.labs.overthewire.org`: Specifies the username (`bandit4`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 4**.

```bash
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
```

#### 3. **Verify the username**:

Check if you are logged in as **bandit5**:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user.

* **Expected output**:

  ```
  bandit5
  ```

#### 4. **List the files in the current directory**:

Use the `ls` command to list the contents of the **inhere** directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.

* **Expected output**:

  ```
  maybehere00  maybehere02  maybehere04  maybehere06  maybehere08  maybehere10  maybehere12  maybehere14  maybehere16  maybehere18
  maybehere01  maybehere03  maybehere05  maybehere07  maybehere09  maybehere11  maybehere13  maybehere15  maybehere17  maybehere19
  ```

You see a series of files named **maybehere00** to **maybehere19**.

#### 5. **Search for the human-readable file**:

Use the `find` command to locate the file that is human-readable and meets the size requirements. We are looking for a file that is not executable and has a specific size.

```bash
find . -type f -size 1033c ! -executable
```

* **Explanation**:

  * `find`: Searches for files in the current directory.
  * `.`: Specifies the current directory as the search location.
  * `-type f`: Searches only for files (not directories).
  * `-size 1033c`: Filters files that are exactly 1033 bytes in size.
  * `! -executable`: Excludes executable files from the search.

* **Expected output**:

  ```
  ./maybehere07/.file2
  ```

This is the file that contains the password.

#### 6. **Read the contents of the file**:

Use the `cat` command to read the contents of **`./maybehere07/.file2`**:

```bash
cat ./maybehere07/.file2
```

* **Explanation**:

  * `cat`: Displays the contents of a file.

* **Expected output**:

  ```
  HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
  ```

This is the password for **Level 5**.

#### 7. **Exit the SSH session**:

Once you have the password for **Level 5**, you can exit the SSH session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Human-readable file**: The file you are looking for is **human-readable**, meaning its contents are not binary or scrambled. By checking the file size and ensuring it is not executable, you can easily locate the correct file.
* **Terminal Reset**: If your terminal becomes garbled or unreadable, you can use the `reset` command to clean up the screen:

  ```bash
  reset
  ```

  This will clear any unwanted characters or formatting issues in your terminal.



# Bandit Level 5 → Level 6

### Level Goal:

The password for the next level is stored in a file somewhere under the **inhere** directory with the following properties:

* Human-readable
* 1033 bytes in size
* Not executable

---

### Commands You May Need:

* `ls`: To list the contents of the current directory.
* `cd`: To change directories.
* `cat`: To display the contents of a file.
* `find`: To search for files or directories.
* `du`: To check disk usage of files and directories.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 5**:

First, use SSH to log into **bandit5** (you should already have the password from **Level 4**).

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit5@bandit.labs.overthewire.org`: Specifies the username (`bandit5`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 5**.

```bash
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

#### 3. **Verify the username**:

Run the `whoami` command to check the current logged-in user:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in username.

* **Expected output**:

  ```
  bandit6
  ```

#### 4. **List the files in the home directory**:

Run `ls` to list the contents of the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists files in the current directory.
    In this case, the directory appears empty.

* **Expected output**:

  ```
  (empty)
  ```

#### 5. **List the files with detailed information**:

Use `ls -la` to see all files, including hidden ones, and their details:

```bash
ls -la
```

* **Explanation**:

  * `ls -la`: Lists all files in the directory, including hidden ones (those that start with a dot), with detailed information like file permissions, owner, and size.

* **Expected output**:

  ```
  total 20
  drwxr-xr-x   2 root root 4096 Oct 14 09:25 .
  drwxr-xr-x 150 root root 4096 Oct 14 09:29 ..
  -rw-r--r--   1 root root  220 Mar 31  2024 .bash_logout
  -rw-r--r--   1 root root 3851 Oct 14 09:19 .bashrc
  -rw-r--r--   1 root root  807 Mar 31  2024 .profile
  ```

In this case, no files appear under the **`bandit6`** user’s home directory, but there are system files like `.bashrc`.

#### 6. **Search for the password file**:

Use the `find` command to locate files that meet the criteria:

* The file is owned by `bandit7` and belongs to the `bandit6` group.
* The file is 33 bytes in size.

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

* **Explanation**:

  * `find`: Searches for files in the system.
  * `/`: Searches from the root directory.
  * `-type f`: Only looks for files (not directories).
  * `-user bandit7`: Finds files owned by the user `bandit7`.
  * `-group bandit6`: Filters for files belonging to the `bandit6` group.
  * `-size 33c`: Searches for files that are exactly 33 bytes in size.
  * `2>/dev/null`: Redirects any error messages to `/dev/null` (essentially silencing errors like "permission denied").

* **Expected output**:

  ```
  /var/lib/dpkg/info/bandit7.password
  ```

This is the file that contains the password for **Level 6**.

#### 7. **Read the contents of the password file**:

Use the `cat` command to read the contents of **`/var/lib/dpkg/info/bandit7.password`**:

```bash
cat /var/lib/dpkg/info/bandit7.password
```

* **Explanation**:

  * `cat`: Displays the contents of a file.

* **Expected output**:

  ```
  morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
  ```

This is the password for **Level 7**.

#### 8. **Exit the SSH session**:

Once you have the password for **Level 7**, you can exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Searching for Specific Files**: The `find` command is very useful for locating files that match certain criteria (e.g., file size, owner, group). In this case, we used it to find a file that is owned by a specific user and group and matches a specific size.
* **File Permissions**: If you are unable to access a file or folder, it's likely due to file permissions. If this happens, you may need to find a different way to access the file or use elevated privileges, depending on the situation.
* **Password Management**: Make sure to save the passwords you find, as they are not stored automatically.


# Bandit Level 6 → Level 7

### Level Goal:

The password for the next level is stored somewhere on the server and has the following properties:

* Owned by user `bandit7`
* Owned by group `bandit6`
* 33 bytes in size

---

### Commands You May Need:

* `ls`: To list the contents of the current directory.
* `cd`: To change directories.
* `cat`: To display the contents of a file.
* `find`: To search for files or directories.
* `grep`: To search for patterns in files.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 6**:

Use SSH to log into **bandit6** using the password you found in **Level 5**.

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit6@bandit.labs.overthewire.org`: Specifies the username (`bandit6`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 6**.

```bash
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

#### 3. **Verify the username**:

Run the `whoami` command to check that you are logged in as **bandit7**:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user.

* **Expected output**:

  ```
  bandit7
  ```

#### 4. **List the files in the home directory**:

Run `ls` to see the files in the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.
    In this case, you should see a file named **`data.txt`**.

* **Expected output**:

  ```
  data.txt
  ```

#### 5. **Search for the password in the file**:

Use the `grep` command to search for the string **"millionth"** in **`data.txt`**. This is likely where the password for **Level 7** is stored.

```bash
grep millionth data.txt
```

* **Explanation**:

  * `grep`: Searches for a specific pattern (in this case, "millionth") within a file.
  * `data.txt`: The file where you are searching for the password.

* **Expected output**:

  ```
  millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
  ```

The password for **Level 7** is **`dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc`**.

#### 6. **Exit the SSH session**:

Once you have the password for **Level 7**, exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Grep Usage**: The `grep` command is handy for searching for specific strings in files. In this case, you used it to search for the string **"millionth"** in **`data.txt`** to locate the password for the next level.
* **File Exploration**: When you found the file **`data.txt`**, it was essential to look for a pattern or clue (like "millionth") that could guide you to the password.


# Bandit Level 7 → Level 8

### Level Goal:

The password for the next level is stored in the file **`data.txt`**, next to the word **"millionth"**. Your task is to extract the password.

---

### Commands You May Need:

* `man`: Displays the manual for a command.
* `grep`: Searches for patterns in files.
* `sort`: Sorts lines of text.
* `uniq`: Filters out duplicate lines.
* `strings`: Extracts printable strings from binary files.
* `base64`: Encodes or decodes data in base64.
* `tr`: Translates or deletes characters.
* `tar`: Archives files.
* `gzip`: Compresses files.
* `bzip2`: Compresses files using the bzip2 algorithm.
* `xxd`: Creates a hex dump of a file.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 7**:

Use SSH to log into **bandit7** (you should already have the password from **Level 6**).

```bash
ssh bandit7@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit7@bandit.labs.overthewire.org`: Specifies the username (`bandit7`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 7**.

```bash
dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
```

#### 3. **Verify the username**:

Run the `whoami` command to check that you are logged in as **bandit8**:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user.

* **Expected output**:

  ```
  bandit8
  ```

#### 4. **List the files in the home directory**:

Run `ls` to see the files in the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.
    You should see a file named **`data.txt`**.

* **Expected output**:

  ```
  data.txt
  ```

#### 5. **Sort the contents of the file and find unique lines**:

Use the `sort` command to sort the contents of **`data.txt`**, and then use `uniq -u` to find the unique lines.

```bash
sort data.txt | uniq -u
```

* **Explanation**:

  * `sort`: Sorts the lines of text in **`data.txt`**.
  * `uniq -u`: Filters the sorted file and displays only the lines that appear once (unique lines).

* **Expected output**:

  ```
  4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
  ```

This is the password for **Level 8**.

#### 6. **Exit the SSH session**:

Once you have the password for **Level 8**, exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Sorting and Uniqueness**: The `sort` and `uniq -u` combination is useful when you're trying to find a unique or non-repeating entry in a file. In this case, the password appeared as a unique line after sorting the content of **`data.txt`**.
* **Password Management**: Be sure to save the password you find, as it will not be stored automatically.






# Bandit Level 8 → Level 9

### Level Goal:

The password for the next level is stored in the file **`data.txt`** and is the only line of text that occurs only once.

---

### Commands You May Need:

* `grep`: Searches for patterns in files.
* `sort`: Sorts lines of text.
* `uniq`: Filters out duplicate lines.
* `strings`: Extracts printable strings from binary files.
* `base64`: Encodes or decodes data in base64.
* `tr`: Translates or deletes characters.
* `tar`: Archives files.
* `gzip`: Compresses files.
* `bzip2`: Compresses files using the bzip2 algorithm.
* `xxd`: Creates a hex dump of a file.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 8**:

Use SSH to log into **bandit8** (you should already have the password from **Level 7**).

```bash
ssh bandit8@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit8@bandit.labs.overthewire.org`: Specifies the username (`bandit8`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 8**.

```bash
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

#### 3. **Verify the username**:

Run the `whoami` command to check that you are logged in as **bandit9**:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user.

* **Expected output**:

  ```
  bandit9
  ```

#### 4. **List the files in the home directory**:

Run `ls` to see the files in the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.
    You should see a file named **`data.txt`**.

* **Expected output**:

  ```
  data.txt
  ```

#### 5. **Extract printable strings from the file**:

Use the `strings` command to extract printable strings from **`data.txt`**:

```bash
strings data.txt
```

* **Explanation**:

  * `strings`: Extracts readable strings from binary files or files that contain mixed data. This will display all printable text in **`data.txt`**.

* **Expected output**:

  ```
  ==========
  the
  ==========
  password
  ==========
  is
  ==========
  FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
  ```

#### 6. **Find the unique line containing the password**:

You can now search for the specific pattern that represents the password using `grep`. The password is the string next to the "====" markers.

Run the following command to search for lines containing **"===="**:

```bash
strings data.txt | grep "===="
```

* **Explanation**:

  * `grep "===="`: Filters the output of `strings` to only show lines that contain the "====" pattern.

* **Expected output**:

  ```
  ==========
  the
  ==========
  password
  ==========
  is
  ==========
  FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
  ```

The password for **Level 9** is **`FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey`**.

#### 7. **Exit the SSH session**:

Once you have the password for **Level 9**, exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Using `strings`**: The `strings` command is very useful for extracting readable text from files that may contain binary data. In this case, it helped us locate the password.
* **Extracting the Password**: The password appears between the "====" markers. By using `grep`, you filtered out only the lines containing the password.

---


# Bandit Level 9 → Level 10

### Level Goal:

The password for the next level is stored in the file **`data.txt`** in one of the few human-readable strings, preceded by several `=` characters. The string is encoded in **base64** and needs to be decoded.

---

### Commands You May Need:

* `grep`: Searches for patterns in files.
* `sort`: Sorts lines of text.
* `uniq`: Filters out duplicate lines.
* `strings`: Extracts printable strings from binary files.
* `base64`: Encodes or decodes data in base64.
* `tr`: Translates or deletes characters.
* `tar`: Archives files.
* `gzip`: Compresses files.
* `bzip2`: Compresses files using the bzip2 algorithm.
* `xxd`: Creates a hex dump of a file.

---

### Solution Step by Step:

#### 1. **Log into Bandit Level 9**:

Use SSH to log into **bandit9** (you should already have the password from **Level 8**).

```bash
ssh bandit9@bandit.labs.overthewire.org -p 2220
```

* **Explanation**:

  * `ssh`: Securely connects to a remote server.
  * `bandit9@bandit.labs.overthewire.org`: Specifies the username (`bandit9`) and the server to connect to.
  * `-p 2220`: Specifies the port number.

#### 2. **Enter the password** when prompted:

Enter the password you found in **Level 9**.

```bash
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```

#### 3. **Verify the username**:

Run the `whoami` command to check that you are logged in as **bandit10**:

```bash
whoami
```

* **Explanation**:

  * `whoami`: Displays the current logged-in user.

* **Expected output**:

  ```
  bandit10
  ```

#### 4. **List the files in the home directory**:

Run `ls` to see the files in the current directory:

```bash
ls
```

* **Explanation**:

  * `ls`: Lists the files in the current directory.
    You should see a file named **`data.txt`**.

* **Expected output**:

  ```
  data.txt
  ```

#### 5. **Decode the base64 file**:

Use the `base64` command to decode **`data.txt`**. The file contains a base64-encoded string that represents the password.

```bash
base64 -d data.txt
```

* **Explanation**:

  * `base64 -d`: The `-d` option decodes the file from base64 format.
  * `data.txt`: The file containing the encoded data.

* **Expected output**:

  ```
  The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
  ```

The password for **Level 10** is **`dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr`**.

#### 6. **Exit the SSH session**:

Once you have the password for **Level 10**, exit the session:

```bash
exit
```

* **Explanation**:

  * `exit`: Ends the current SSH session and logs you out.

---

### Notes:

* **Base64 Encoding**: The password was stored in base64 format, which is a common encoding scheme. The `base64 -d` command decodes the file into its original, human-readable format.
* **Password Management**: Make sure to save the password you find, as it will not be stored automatically.

---
