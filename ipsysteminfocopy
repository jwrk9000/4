#opens powershell, finds ip, copies it to folder on desktop
#also logs system into to a text file on desktop
#requires admin permission

import os

# Open PowerShell and run the "ipconfig" command
result = os.popen("powershell ipconfig").read()

# Find the IPv4 address in the output
ipv4 = [line for line in result.split("\n") if "IPv4" in line][0].split(":")[1].strip()

# Create the destination folder (on the desktop) if it doesn't exist
folder = 'C:\\Users\\User\\Desktop\\IP_Address'
if not os.path.exists(folder):
    os.makedirs(folder)

# Write the IPv4 address to a text file in the destination folder
with open(f"{folder}/ip_address.txt", "w") as file:
    file.write(ipv4)

# Open PowerShell and run the "systeminfo" command
result = os.popen("powershell systeminfo").read()

# Create the destination folder (on the desktop) if it doesn't exist
folder = 'C:\\Users\\User\\Desktop'
if not os.path.exists(folder):
    os.makedirs(folder)

# Write the results to a text file on the desktop
with open(f"{folder}/systeminfo.txt", "w") as file:
    file.write(result)
