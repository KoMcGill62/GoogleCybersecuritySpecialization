# This is a brief summary of what skills this lab project taught me and my understanding of python

## The goal of this code is to open the file that contains the allow list
<img width="512" height="333" alt="image" src="https://github.com/user-attachments/assets/290c4449-7006-41d3-8428-47aa2f0cc197" />

import_file = "allow_list.txt"

In the first line of code the goal is to assign the "allow_list.txt" file name as a string with the variable "import_file".

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

The second line is just another variable with a list of necessary IP's to complete the lab.

## The goal here is to read the file contents
<img width="512" height="72" alt="image" src="https://github.com/user-attachments/assets/b3b8d756-0470-454a-be55-49ae9b5a6e12" />

with open(import_file, "r") as file:

Here I use a ‘with’ statement with the .open() function that includes an “r” argument to signal I want to read. 

ip_addresses = file.read()

The .read() function converts it to a string and I applied it to the file variable. I also assigned the string output of this method to the variable “ip_addresses”.

## The goal here is to convert the string into a list
<img width="512" height="37" alt="image" src="https://github.com/user-attachments/assets/eaa14905-34dd-42e9-ab51-d29fea521211" />

ip_addresses = ip_addresses.split()

The split function is used in this example by attaching it to the "ip_addresses" variable. The purpose of splitting this in the lab was to make it easier to remove IP addresses from the allow list. The split() function acts by taking the data stored and separating it by white spaces. The list was then reassigned back to the original variable.

## The goal here is to iterate through the remove list
<img width="256" height="96" alt="image" src="https://github.com/user-attachments/assets/1d9a0773-3c29-4ad2-b712-e8426cda33fa" />

for element in remove_list:

The for loop acts by repeating the code for the upcoming sequence. The loop variable is 'element' and using the keyword in shows which list the loop needs to occur in.

## The goal is to remove IP addresses that are on the remove list
<img width="512" height="96" alt="image" src="https://github.com/user-attachments/assets/0640e258-b0fb-4daa-a172-9d9f0f4b3e7f" />

for element in ip_addresses:

The code starts with a for loop that searches for the variable 'element' in the 'ip_addresses' list.

if element in remove_list:

The second line uses an 'if' statement to find if the element also exists in the 'remove_list'. I used the remove() function to direct if the element is in the list to remove it from 'ip_addresses'.

ip_addresses.remove(element)

In the last line I use the remove() function to direct if the element is in the list to remove it from 'ip_addresses'.

## The goal is to update the file with the revised list of IP addresses
<img width="451" height="64" alt="image" src="https://github.com/user-attachments/assets/9e56eb38-8664-4092-9c65-fb1ac522d2d6" />

ip_addresses = "/n".join(ip_addresses)

The join method combines everything after the =sign into one string. I used the .join() function to create a string from the list 'ip_addresses' and I used the "/n" as the separator to make sure each element is on its own line.

<img width="500" height="72" alt="image" src="https://github.com/user-attachments/assets/920c046c-a6cd-4685-a7ee-d163b1f3bfa3" />

with open(import_file, "w") as file:

I used another with statement with the open() function with the argument "w" to signal I want to write over the current contents. 

file.write(ip_addresses)

In this lab I want to update the allow list and make it a string assigned to "allow_list.txt". I rewrote this file and appended the .write() function to the file object file that was identifed from the with statement. I then used the "ip_addresses" variable as the argument to specify that the with statement should be replaced with this variable.
