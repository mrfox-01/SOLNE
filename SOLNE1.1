import fileinput
import tkinter
from tkinter import filedialog
from multiprocessing.connection import _ConnectionBase, Connection
from datetime import datetime
from sqlite3 import connect
from netmiko import ConnectHandler
import os

os.system('cls')
now = datetime.now()
date_now = now.strftime("%m%d%Y")
backupDir = "BACKUP"+date_now

print("   _____  ____  _      _   _ ______ ")
print("  / ____|/ __ \| |    | \ | |  ____|")
print(" | (___ | |  | | |    |  \| | |__   ")
print("  \___ \| |  | | |    | . ` |  __|  ")
print("  ____) | |__| | |____| |\  | |____ ")
print(" |_____/ \____/|______|_| \_|______| v1.1")
print()

print("This version can only backup cisco appliances, more things to come :)")
print()
print("Choose a location for the backup folder")
input("Press Enter to choose a location...")

#choosing where to save backups
tkinter.Tk().withdraw()
savePath = filedialog.askdirectory()
backupPath = savePath+"/"+backupDir #test file location
isExist = os.path.exists(backupPath)
if not isExist:
    os.mkdir(backupPath)

#print("Do you have a host file? y/n")
print("Choose the host file containing the devices IP's")
input("Press enter to choose host file...")

#obtain IPs from hosts.txt file
tkinter.Tk().withdraw()
folderPath = filedialog.askopenfile()
hostList = folderPath.readlines()

#requesting creds from user for appliances
username = input("Please input SSH username: ")
password = input("Please input SSH password: ")
secret = input("Please specify secret: ")
print()
os.system("cls")

print('Generating backups...')

#commands for appliance backup
backup_commands = ['show logging','show vlan brief','show vtp status','show cdp neighbor' ,'show cdp neighbor detail' ,'show ver' ,'show switch detail' ,'show switch stack-ports' ,
'show ip int brief | ex unass' ,'show power inline | ex off' ,'show interface description' ,'show int status' ,'show int stat' ,'show int status | i sus' ,'show int status | I err' ,
'sh mac address-table' ,'show ip arp' ,'show env all' ,'show inventory' ,'show run']

for host in hostList:

    appliance = {
    "device_type": "cisco_ios",
    "host": host, #ip of devices
    "username": username, #username
    "password": password, #password 
    "secret": secret #secret
    }

    connection = ConnectHandler(**appliance) # unpacking the dictionary
    connection.enable()

    #obtain hostname of appliance
    show_hostname = connection.send_command("show run | i hostname")
    hostname_split = show_hostname.split(" ")
    hostname = hostname_split[1]

    file_name = hostname + "_" + date_now + ".txt"
    filePath = (backupPath + '/' + file_name)
    file = open(filePath, 'w')

    for command in backup_commands:
        file.write(command+"\n")
        file.write(connection.send_command(command) + "\n")
        file.write("\n")
    print("\nFile '" + file_name + "' has been created.\n")
    file.close




