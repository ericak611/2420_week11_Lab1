# Week 11 Lab 
Anjana Jayakody / Hyewon Kim 

# Moving files from local to remote server

1. Open the terminal
2. Type > wsl
3. cd into the directory you would like to transfer files to remote server

   ![Directory!](./images/directory.JPG)

4. Using the remote server user and ip address sftp into it.
   e.g., > sftp user@ipaddress 

   ![sftp!](./images/sftp.JPG)

5. Upload the directory from host machine to remote server by typing the following command.
   e.g., > put -r directory-name.

   ![upload!](./images/upload.JPG)

6. Check the remote server in /home/user-name to see if the directory is uploaded.

   ![check!](./images/check.JPG)

#  Moving files to appropriate directory 

1. Copy the script file to the path where you have specified to execute in the service file. 
   e.g., > sudo cp directory-script/script destination/path 

   ![copy_script!](./images/copy_script.JPG)

2. Copy the service and timer files to /etc/systemd/system/
   e.g., > sudo cp directory-name/script.service /etc/systemd/system/ 

   ![copy!](./images/copy.JPG)

3. Change permission so that the script is executable 
   e.g., > sudo chmod +x path
   
   ![permission!](./images/permission.JPG)

4. Run the command > sudo systemctl daemon-reload
5. Start the service by running the command > sudo systemctl start script-name.service
6. Check to see if it is working by running the command > sudo systemctl status script-name.service

   ![working!](./images/working.JPG)

7. Enable the service by running the command > sudo systemctl enable --now script-name
8. Enable the timer by running the command > sudo systemctl enable --now script-name.timer 
9. Check to see if the timer is working by running the command > sudo systemctl list-timers  
   
   ![list_timer!](./images/list_timer.JPG)
   
   ![list_output!](./images/list_output.JPG)
   
   ![timer_working!](./images/timer_working.JPG)
