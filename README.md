<h1>Updating a File</h1>


<h2>Description</h2>
At my organization, access to restricted content is controlled with an allow list of IP addresses.The "allow_list.txt" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. I created an algorithm to automate updating the "allow_list.txt" file and remove these IP addresses that should no longer have access.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Python</b> 

<h2>Environments Used </h2>

- <b>Python Notebook</b> 

<h2>Program walk-through:</h2>

<p align="center">
Open the file with the allow list: For the first part of the algorithm, I opened the "allow_list.txt" file. First, I assigned this file name as a string to the import_file variable: <br/>
<img src="https://imgur.com/eBbZYyt.png" height="80%" width="80%" alt="Updating Steps"/>
<br/>
Then, I used a with statement to open the file:
<img src="https://imgur.com/a2u93Wa.png" height="80%" width="80%" alt="Updating Steps"/>
<br />
Read file content:  <br/>
<img src="https://imgur.com/JJAjH8h.png" height="80%" width="80%" alt="Updating Steps"/>
<br />
Convert the string into a list: In order to remove individual IP addresses from the allow list, I needed it to be in list format <br/>
<img src="https://imgur.com/nrTBkEe.png" height="80%" width="80%" alt="Updating Steps"/>
<br />
Iterate through the remove list:  <br/>
<img src="https://imgur.com/w61F0Ka.png" height="80%" width="80%" alt="Updating Steps"/>
<br />
Remove IP addresses that are on the remove list:  <br/>
<img src="https://imgur.com/6xNUBfT.png" height="80%" width="80%" alt="Updating Steps"/>
<br />
Update the file with the revised list of IP addresses: To do so, I first needed to convert the list back into a string. I used the .join() method for this:  <br/>
<img src="https://imgur.com/HHrFreC.png" height="80%" width="80%" alt="Updating Steps"/>
<br/>
Then, I used another with statement and the .write() method to update the file:  <br/>
<img src="https://imgur.com/WVfk5oj.png" height="80%" width="80%" alt="Updating Steps"/>
<br/>
Summary: I created an algorithm that removes IP addresses identified in a remove_list variable from the "allow_list.txt" file of approved IP addresses. This algorithm involved opening the file, converting it to a string to be read, and then converting this string to a list stored in the variable ip_addresses. I then iterated through the IP addresses in remove_list. With each iteration, I evaluated if the element was part of the ip_addresses list. If it was, I applied the .remove() method to it to remove the element from ip_addresses.. After this, I used the .join() method to convert the ip_addresses back into a string so that I could write over the contents of the "allow_list.txt" file with the revised list of IP addr  <br/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
