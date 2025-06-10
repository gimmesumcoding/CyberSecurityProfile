Algorithm for file updates in Python

PROJECT DESCRIPTION

You are a security professional working at a health care company. As part of your job, you're required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees you must remove from this allow list.

Your task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, you should remove those IP addresses from the file containing the allow list.

OPEN THE FILE THAT CONTAINS THE ALLOW LIST

# Assign the file name to the variable

import_file = "allow_list.txt"

# Use a with statement to open the file

with open(import_file, "r") as file:

READ THE FILE CONTENTS

 # Read the contents of the file as a string

    ip_addresses = file.read()

CONVERT THE STRING INTO A LIST

# Use '.split()' to convert the string into a list of individual IP addresses

ip_addresses = ip_addresses.split()

ITERATE THROUGH THE REMOVE LIST

# Build conditional statement
# If current element is in 'remove_list'

if element in remove_list:

  # Check if the element is in the current IP address list

  if element in ip_addresses:

REMOVE IP ADDRESSES THAT ARE ON THE REMOVE LIST

# Use 'remove()' to remove the current element from 'ip_addresses'

ip_addresses.remove(element)

UPDATE THE FILE WITH THE REVISED LIST OF IP ADDRESSES

# Convert list back to string format with newline between each IP

ip_addresses = "\n".join(ip_addresses)

# Write the updated list back to file

with open(import_file, "w") as file:
    file.write(ip_addresses)

SUMMARY

This project demonstrates my ability to automate file processing using Python. I created a script that updates a security access file by removing outdated or unauthorized IP addresses from an allow list. The allow list is stored in a text file, and the script ensures that only approved IPs remain by comparing the list to a predefined set of IPs to remove. This solution is useful for system administrators or security analysts who need to maintain up-to-date access control files efficiently. All file operations were handled using Python's with statement and list manipulation techniques.

The algorithm starts by reading the contents of a text file containing IP addresses using the .read() method and storing the data as a string. It then converts the string into a list using the .split() method so that individual IP addresses can be managed. Next, the script iterates through a removal list, and any IP address found in both lists is removed from the main IP list using the .remove() method. This is safe to do because the original list does not contain duplicates. After cleaning the list, it is converted back into a newline-separated string using "\n".join() to maintain formatting. Finally, the updated list is written back to the original file, replacing the old contents entirely with the cleaned data.
