# Blue-Team-Log-Analysis

### Log Analysis and Attack Characterization

ELK received logs of an *icmp* port scan directed at ip 192.168.1.105.
A large amount of icmp packets in a short amount of time is indicative of a port scan.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/port_scan_flood.png "Port_Scan_Flood")
 
An unusual amount of unauthorized *GET* request for the ./secret_folder was noticed.  

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/unusual_get_requests.png "Unusual_Get_Requests")

Further analysis of the mentioned GET requests revealed a *Hydra* signature.
*Hydra* is a publicly-available, login cracker.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/hydra_signature.png "Hydra_Signature")

Within a few minutes, the ./secret_folder received a total of 40,675 queries.
Below depicts the moment the /secret_folder login page is succesfully accessed.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/brute_force_to_secret_folder.png "Brute_Force_To_Secret_Folder")

A successful query was made for a file ./connect_to_corp_server, which contains sensitive information. 

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/sensitive_file_get_requested.png "Sensitive_File_Get_Requested")

The next day a suspicious file was uploaded to the ./webdav Index.

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/uploaded_file_to_company_server.png "Uploaded_File")

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/put_request_of_suspicious_file.png "Put_Request")

After the uploaded file was accessed, traffic was detected going back to the same ip that was involved in the port scan and brute force attempt. 

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/suspicious_file_opened_by_attacker.png "File_Opened_By_Attacker")

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Blue-Team-Images/outbound_traffic_to_suspicious_ip.png "Outbound_Traffic")

### Mitigation

#### Consider onboarding a full time cyber analyst to conduct log analysis and propose system hardening. 














