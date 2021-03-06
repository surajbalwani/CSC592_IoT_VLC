Host1 Code: 
Reader.py
To execute run: python Reader.py 

Host1 establishes TCP connection with RaspberryPi.
When the server on the RaspberyPi is running, it displays a port number on which it is listening for 'data'.
When the Host 1 code is executed, this port number must be entered as the server port.

Host1 reads data from file/from user input (as per option selected) and sends this data bytewise to RaspberryPi.

User options:

0 : User input
	Input is taken from the user on the terminal, and can be seen in real-time on the terminal running on Host 2.
	Our application has support for characters such as 'Enter','Tab' and 'Backspace', but not for 'Arrow keys'.
	The 'ESC' key is used as the termination character on Host 1.

1 : Read from file
	Data is read from a file that is present in the same working directory as Reader.py. Any type of file can be sent
        across this link, and can be perfectly reconstructed on Host 2, as long as the correct file extension is given.
        The file name is taken as an input from the user.

NOTE - Do not start transmission of either type on Host 1 until Host 2 has also connected to the server on the RaspberryPi.
       In case of file transfer, the filename must also be entered on Host 2 before entering the value '1' on Host 1.
       After starting the process on Host2, you will need to wait for 1 second before starting transmission from Host1.
       This is to give the serial channel between the Arduino and Host 2 some time to settle.




