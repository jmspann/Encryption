<h1>Encryption and Decryption</h1>

<h2>Description</h2>
This lab focuses on encryption and decryption of files for added security within an organization's file management. This lab will utilize hashing files for encryption and data integrity, and recovering data using decryption techniques.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux Command-Line</b> 

<h2>Environments Used </h2>

- <b>KALI LINUX</b>
- <b>Linux Bash Shell</b>

<h2>Program Walk-Through:</h2>

<h3>Hashing Files</h3>

<p align="center">
In the "analyst" directory there are 2 files located called "file1.txt" and "file2.txt". These two files contain different data, however when both file is opened, they appear the same. We'll first start by creating a hash value for each file using the <em><strong>SHA256SUM</strong></em> command: <br/>
<img src="https://i.imgur.com/yzF02kD.png" height="100%" width="100%" alt="Hashing Files"/>
<br />
<br />
Next, we'll save each hash value into a separate file:  <br/>
<img src="https://i.imgur.com/f6NqUBN.png" height="100%" width="100%" alt="Hashing Files"/>
<br />
<br />
Now we can compare the hashes using the <em><strong>cmp</strong></em> command. The output shows us that the two hashes are different, therefore the two original files - "file1.txt" and "file2.txt" - are different: <br/>
<img src="https://i.imgur.com/udEmHXL.png" height="100%" width="100%" alt="Hashing Files"/>
</p>
<br />
<br />

<h3>Decrypt a File Using a Caesar Cipher</h3>

<p align="center">
In our "analyst" directory, we have an encrypted file ("Q1.encrypted") that we want to access, but in order to we have to decrypt it. By opening the "README.txt" file, we find that the decryption key is in the "caesar" subdirectory:  <br/>
<img src="https://i.imgur.com/nroUXxe.png" height="100%" width="100%" alt="Decryption"/>
<br />
<br />
Find the hidden file in the "caesar" subdirectory and read its contents:  <br/>
<img src="https://i.imgur.com/PtzHjZL.png" height="100%" width="100%" alt="Decryption"/>
<br />
<br />
<p align="center">
The message in the ".leftShift3" hidden file is scrambled using a caesar cipher. This one can be solved by shifting every letter 3 letters to the left. In order to do this, we need to reopen the file and translate every letter by inputting <em><strong>| tr "d-za-cD-ZA-C" "a-zA-Z"</strong></em>:  <br/>
<img src="https://i.imgur.com/x42aboz.png" height="100%" width="100%" alt="Decryption"/>
<br />
<br />
The hidden file revealed a command we can use to decrypt our files. We need to return to our home directory and execute the command, which will create a new file called "Q1.recovered". We can see if it worked by opening the file and reading the enclosed message:  <br/>
<img src="https://i.imgur.com/opEqbkO.png" height="100%" width="100%" alt="Decryption"/>
</p>
<br />
<br />
