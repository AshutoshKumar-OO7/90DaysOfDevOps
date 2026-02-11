*Environment Basics

  Command-# Uname -a

  <img width="1733" height="149" alt="uname -a" src="https://github.com/user-attachments/assets/9dd17d60-bbaf-4b98-9f7b-479a77b01d8f" /> All information about Kernel versiom

  Command-# cat /etc/os-release

  <img width="1044" height="431" alt="OS release" src="https://github.com/user-attachments/assets/32da527e-0127-4985-99ae-6a026d2027b3" /> Distribution and Release Version

*FileSystem sanity

  Command-# mkdir /tmp/runbook-demo

  <img width="1452" height="396" alt="mkdir" src="https://github.com/user-attachments/assets/871d0001-49d4-4a2e-afb9-056e42caf223" /> Dirctory Created Successfully

  Command-# cp /etc/hosts /tmp/runbook-demo/hosts-copy && ls -l /tmp/runbook-demo

  <img width="928" height="211" alt="cp and ls -l" src="https://github.com/user-attachments/assets/d56c290e-f812-456c-9a91-85610eb7b7df" /> Copied the files from /etc/hosts.

*CPU/Memory 

  Command-# Top , htop & free -h

  <img width="1920" height="1007" alt="top" src="https://github.com/user-attachments/assets/572b2195-9703-4612-9950-eb2e79051d71" /> Tasks-42 Running-1 Sleeping-41
  <img width="1920" height="1024" alt="htop" src="https://github.com/user-attachments/assets/4f5b48e8-baea-4a1a-9173-c7e79e74546d" />
  <img width="1000" height="180" alt="free -h" src="https://github.com/user-attachments/assets/4ca4f57b-bdda-448d-bc40-47a54fbbc329" />
  Sufficient memory available.

  Command-# ps -o pid,pcpu,pmem,comm -p 1-2

  <img width="735" height="320" alt="ps -o pid" src="https://github.com/user-attachments/assets/3d9989e7-8323-463b-857b-b87ef4a30ff4" />

*Disk/ IO

 Command-# iostat , vmstat , dstat

 <img width="894" height="688" alt="dstat" src="https://github.com/user-attachments/assets/417e351e-975e-4f61-b715-c8568fe8f004" />
 <img width="1382" height="521" alt="vmstat iostat" src="https://github.com/user-attachments/assets/8f1fbe5d-8309-460c-9e99-9d674ac2c9e1" />

 Command-# df -h, du -sh /var/log

 <img width="1121" height="524" alt="df -h" src="https://github.com/user-attachments/assets/103b1a3d-a010-4f52-8f70-db5108a2857f" /> more than 90% available.
  
  <img width="625" height="165" alt="du -sh" src="https://github.com/user-attachments/assets/162cdfc0-0c19-4bc8-8603-b77106b0619d" />

*NetWork

  Command-# ss -tulip

  <img width="1920" height="442" alt="ss -tulpn" src="https://github.com/user-attachments/assets/ffdc3161-a061-4a08-9ee8-b18d3598c622" />

  Command-# netstat -tulip

  <img width="1221" height="514" alt="netstat -tulpn" src="https://github.com/user-attachments/assets/8f1ec217-734c-49f9-af76-c6437e515aa5" />

*Logs

   Command-# journalctl -u docker -n 50

   <img width="1920" height="1017" alt="journalctl" src="https://github.com/user-attachments/assets/aa87560c-431a-4430-8839-61ab0f2b4751" />

 
 





