# CLI_practice
practice files

File 1:  status_log.txt

2025-12-01: INFO - System initialization complete.
2025-12-01: ERROR - Failed to connect to server 192.168.1.1. Retrying...
2025-12-02: INFO - User session opened successfully.
2025-12-02: WARNING - Disk space usage at 85%. Review needed.
2025-12-03: INFO - Backup process initiated.
2025-12-03: ERROR - Data integrity check failed on volume /dev/sdb.
2025-12-04: INFO - System check passed.

Exercises:

grep ERROR status_log.txt - Find lines containing the word ERROR.

grep INFO status_log.txt - Find all successful information messages.

wc -l status_log.txt - Count the total number of lines (log entries).



File 2:  credentials.bak

# Configuration Backup (Do not expose!)
Username=admin_user
Hash=f87d46b8c9e54a01c34a23b56
Service_URL=https://api.internal.network/v1
Timeout=600
Port=8080

Exercises:

head -n 2 credentials.bak - View only the first 2 lines of the file.

tail -n 1 credentials.bak - View only the last line (the Port).

cat credentials.bak - Display the entire file content to the screen.



File 3:  sales_data.csv

Product,Region,UnitsSold,Revenue
Laptop_Pro,East,25,125000
Monitor_4K,West,102,40800
Keyboard_RGB,Central,500,25000
Mouse_Laser,East,80,4000
Laptop_Base,West,12,60000
Webcam_HD,Central,350,17500

Exercises: 

sort -t, -k3 -n sales_data.csv - Sort the data numerically (-n) based on the third field (-k3), using the comma (,) as the field delimiter (-t,). This sorts by UnitsSold.

`sort -t, -k4 -n sales_data.csv - tail -n 1`

grep East sales_data.csv - Filter the entire file to show only records from the "East" region.



File 4:  cleanup_text.cfg

server_name:web01;ip_address:10.0.0.1;status:running
server_name:db02;ip_address:10.0.0.2;status:halted
server_name:cache03;ip_address:10.0.0.3;status:running
server_name:backup04;ip_address:10.0.0.4;status:running

Excercises: 

`cat cleanup_text.cfg - tr ';' '\n'`

`grep halted cleanup_text.cfg - cut -d: -f2`

wc -w cleanup_text.cfg - Count the total number of words in the configuration file.



File 5:  duplicate_users.list

user_alice
user_bob
user_charlie
user_bob
user_david
user_alice
user_alice
user_david
user_charlie
user_bob

Exercises:

`sort duplicate_users.list - uniq`
`sort duplicate_users.list - uniq -c`
`sort duplicate_users.list - uniq -c
