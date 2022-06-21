# Blue-Team-Log-Analysis

### Log Analysis and Attack Characterization

ELK received logs of an *icmp* port scan directed at ip 192.168.1.90.
A large amount of icmp packets in a short amount of time is indicative of a port scan.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/port_scan_flood.png "Port_Scan_Flood")
 
An unusual amount of unauthorized *GET* request for the ./secret/folder was noticed.  

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/unusual_get_requests.png "Unusual_Get_Requests")

Further analysis of the mentioned GET requests revealed a *Hydra* signature.
*Hydra* is a publicly-available, login cracker.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/hydra_signature.png "Hydra_Signature")

Within a few minutes, the ../secret_folder received a total of 40,675 queries.
Below depicts the moment the /secret_folder login page is succesfully accessed.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/brute_force_to_secret_folder.png "Brute_Force_To_Secret_Folder")

A successful query was made for a file ../connect_to_corp_server, which contains sensitive information. 

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/secret_file_get_requested.png "Secret_File_Get_Requested")


![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/.png "")







