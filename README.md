# Red-Team-vs-Blue-Team
Results of fulfilling both red team and blue team roles. 

Figure 1 depicts the environment topology which includes 3 machiens with the folowing configurations:

| Name        | Function                                  | IP            |
|-------------|-------------------------------------------|---------------|
| Kali Linux  | Conduct a penetration test.               | 192.168.1.90  |
| Capstone VM | Serve as a vulnerable virtual machine.    | 192.168.1.100 |
| ELK Server  | Receives log information from Capstone VM | 192.168.1.105 |

________


Tools

Kali Linux:

- Hydra
- Nmap
- John the Ripper
- Metasploit
- curl
- MSFvenom

Capstone Vm

- Filebeat 
- Metricbeat
- Packetbeat

ELK Server

- Elasticsearch
- Logstash
- Kibana
