# This is a brief summary of what skills this lab project taught me and my understanding of python

## The goal of this code is to open the file that contains the allow list
<img width="512" height="333" alt="image" src="https://github.com/user-attachments/assets/290c4449-7006-41d3-8428-47aa2f0cc197" />

import_file = "allow_list.txt"

In the first line of code the goal is to assign the "allow_list.txt" file name as a string with the variable "import_file".

remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

The second line is just another variable with a list of necessary IP's to complete the lab.

## The goal here is to read the file contents
<img width="512" height="72" alt="image" src="https://github.com/user-attachments/assets/b3b8d756-0470-454a-be55-49ae9b5a6e12" />

with open(import_file, "r"0 as file:

Here I use a ‘with’ statement with the .open() function that includes an “r” argument to signal I want to read. The .read() function converts it to a string and I applied it to the file variable. I also assigned the string output of this method to the variable “ip_addresses”.
