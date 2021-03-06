# Monitor and Exploit a Server
Results of fulfilling both red team and blue team roles. 

Figure 1 depicts the environment topology which includes 3 machines with the following configurations:

| Name        | Function                                  | IP            |
|-------------|-------------------------------------------|---------------|
| Kali Linux  | Conduct a penetration test.               | 192.168.1.90  |
| Capstone VM | Serve as a vulnerable virtual machine.    | 192.168.1.100 |
| ELK Server  | Receives log information from Capstone VM.| 192.168.1.105 |

![alt-text](https://github.com/Travis-Dominguez/Red-Team-vs-Blue-Team/blob/main/Images/Network_Topology_1.png "Network_Topology")


Tools

Kali Linux:

- Hydra
- Nmap
- John the Ripper
- Metasploit
- Curl
- MSFvenom

Capstone Vm

- Filebeat 
- Metricbeat
- Packetbeat

ELK Server

- Elasticsearch
- Logstash
- Kibana
