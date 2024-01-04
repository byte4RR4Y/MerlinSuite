# MerlinSuite
-------------------------------------------------------------------------------------------------------------
# A Command and Control (C2) Framework, with teamserver and clients
# with Advanced Features for Windows, Linux, MacOS, and rooted android(requires terminal like Termux)

In today's digital world, the development of Command and Control (C2) frameworks has become a significant
aspect of cybercrime and security research. These frameworks offer the ability to control and monitor computer
and network systems, and are of great interest to malicious actors and security experts alike. This essay
explores a C2 framework that offers various advanced features, including upload and download functions,
browser data theft, keylogger functionality, webcam access, ransomware capability, automatic port-forwarding
tunnels through the Tor network, and a zip function for files and folders.

1. **TLS Configuration:**
   - The program generates a TLS configuration to secure the communication between the server and clients.

2. **Credentials Handling:**
   - User credentials (username and password) are stored in a `config.json` file.
   - The `readCredentials` function retrieves credentials based on the provided username.

3. **Environment Variables and Configuration:**
   - The program reads environment variables from a `.env` file or prompts the user for values if they are not set.
   - The `generateTLSConfig` function creates TLS certificates for secure communication.

4. **Interactive Session Management:**
   - The program supports multiple reverse connections, each represented by a `ReverseSession` struct.
   - It maintains a list of active and inactive reverse connections.
   - Users can interact with active reverse connections through a menu system.
   - Authentication is performed using a username/password combination.
   - The `serverMenu` function provides a menu for interacting with the reverse connections.

5. **File Transfer:**
   - Clients can download files from the remote host using the `download` command.
   - Clients can upload files to the remote host using the `upload` command.

6. **HTTP Server:**
   - An HTTP server is started to serve files from the "payload" directory.

7. **Dynamic Loading of Environment Variables:**
   - Users can choose to load old environment variables from a previous `.env` file.

8. **Client Communication:**
   - The program listens for both client and reverse connections simultaneously.

9. **Command Execution:**
   - The program supports executing arbitrary commands on connected clients.
   - Specific commands are tailored for different operating systems (Windows and Linux).

10. **Security Measures:**
    - The program checks for existing users and prevents multiple logins with the same credentials.
    - TLS is used to encrypt communication between the server and clients.

11. **Port Scanning:**
    - Clients can initiate port scans using the `portscan` command.

12. **File Compression:**
    - Clients can compress files or folders using the `compress` command.

13. **Help Menu:**
    - Clients can access a help menu (`help` command) to understand available commands.

14. **Additional Features:**
    - The program has features like keylogger management, browser data stealing, and more.
    - There are commands for installing software (e.g., Python, Winget) on Windows clients.

15. **Concurrent Execution:**
    - Goroutines are used for concurrent execution of various tasks.

16. **File Encryption and Patching AMSI:**
    - The program includes commands for file encryption and patching the AMSI (Anti-Malware Scan Interface) on Windows.

17. **Web Server for File Retrieval:**
    - An HTTP server is started to serve files from the "payload" directory.

18. **Dynamic IP Configuration:**
    - The server allows dynamic configuration of IP addresses through user input or environment variables.

19. **Remote OS Detection:**
    - The server attempts to detect the operating system of connected remote hosts.


# SESSION COMMANDS:
-------------------------------------------------------------------------------------------------------
download <filename>                  e.g.: download picture.jpg
upload <absolute_path_to_file>       e.g.: upload /home/user/Pictures/picture.jpg
keylogger start                      Starts keylogger [requires python]
keylogger download                   Downloads the keys.txt file from keylogger
compress <filename/foldername>       compress file or folder, can't zip empty folders
install winget                       [ON WINDOWS]
install python                       [ON WINDOWS] [requires winget]
steal browserdata1                   Sometimes not working, but works on all browsers.
steal browserdata2                   [ON WINDOWS]all browsers, except firefox [requires python]
steal firefox                        [ON WINDOWS]steal passwords from firefox [requires python]
portscan <IPRange> <PortRange|List>  portscanner 1.0.0.0-1.1.255.255 1-1024 or 1,2,3
encrypt files                        encrypts all user files,downloads encryption_key
patch amsi                           [ON WINDOWS] Patch the AMSI for the current Session
back                                 back to main menu
-------------------------------------------------------------------------------------------------------

The Listener runs on port 4443
The port for downloading files is 55555
The Webserver runs on port 8080
(no sudo rights are neccesary to run the program, only on installation)

# Video at t.me/exploiting_systems
and website with vide
# https://19cb-2a09-bac5-2aa2-18fa-00-27d-37.ngrok-free.app
