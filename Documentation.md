We start off by connecting to the database and check what smokey has.

<img width="776" height="286" alt="Screenshot 2026-03-06 165027" src="https://github.com/user-attachments/assets/68c63ef0-14c0-431d-a64f-4b1017b9fa9d" />

We see the password and run nmap to check for additional open ports for access to the database.

<img width="791" height="325" alt="Screenshot 2026-03-06 170000" src="https://github.com/user-attachments/assets/46ffd0c6-5e24-4f27-98f5-f343c99ab22f" />

We try to ssh into the database but the password is not for it.

However if we look back at the netcat connection we can see that the input accepts a certain amount of sqlite commands but most commands would be blocked in this sort of connection so we try something else like changing the case sensitivity of the commands to trick the database to run commands. (Lots of trial and error to figure out which commands will and wont work.)

<img width="778" height="263" alt="Screenshot 2026-03-06 175617" src="https://github.com/user-attachments/assets/e8f1bb78-b614-4e65-bb10-8b363836bc2e" />

We can run this command to find the different tables in the database. We found admintables so we can then run something to get the data.

<img width="857" height="152" alt="Screenshot 2026-03-06 175651" src="https://github.com/user-attachments/assets/b7018969-4db7-4eb5-ab2d-cb4fadf18415" />
