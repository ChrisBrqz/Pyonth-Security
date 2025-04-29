# Python-Security
This project automates the process of managing an IP allow list by removing unauthorized IP addresses using Python. It simulates a real-world task where a security analyst ensures only approved users retain access to a protected network.

Project Description
In a simulated healthcare setting, employees are granted access to a restricted network based on their IP addresses. The access is managed through an `allow_list.txt` file. To maintain security compliance, IPs listed in a `remove_list` must be revoked.



This Python script:
- Reads a file of currently authorized IPs (`allow_list.txt`)
- Cross-checks it with a `remove_list` of revoked IPs
- Removes matching IPs from the allow list
- Rewrites the updated list back to the original file

How It Works
1. Loads the allow list from a `.txt` file
2. Splits IPs into a list format
3. Iterates through the list and removes any IPs found in `remove_list`
4. Saves the updated list back to the file

Technologies Used
- Python 3
- File I/O
- List operations
- Basic string parsing

## Files
- `allow_list.txt` – List of currently authorized IP addresses
- Python script – Automates IP list cleanup

## Sample Code

python
remove_list = ["192.168.97.225", "192.168.158.170", "192.168.201.40", "192.168.58.57"]

with open("allow_list.txt", "r") as file:
    ip_addresses = file.read().split()

ip_addresses = [ip for ip in ip_addresses if ip not in remove_list]

with open("allow_list.txt", "w") as file:
    file.write(" ".join(ip_addresses))

    // This project demonstrates how Python can be used in cybersecurity roles to automate repetitive but critical security tasks. It highlights key skills like data validation, secure access control, and file manipulation.
