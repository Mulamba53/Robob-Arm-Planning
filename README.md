 Robot Arm Project
 Description: For this assignement we were supposed to create a robot arm using onshape and the printing it out using the 3d printer.
 Images_-_ ![image](https://github.com/Mulamba53/engineering3/assets/143534921/deef163e-d7a9-4eba-ba79-eed9a053297f)
 ![image (1)](https://github.com/Mulamba53/engineering3/assets/143534921/28c31280-edbf-45a6-923a-e1e72d3355e8)

Part Link--https://cvilleschools.onshape.com/documents/4461ea2583dd0b40fb8d2c30/w/cf3f42276d29b4e586c902cb/e/68235954af8c765a65d31feb
Coding--import serial
import time

# Define the serial port and baud rate
serial_port = 'COM3'  # Change this to the appropriate serial port
baud_rate = 9600  # Make sure it matches the baud rate of your device

# Create a serial connection
ser = serial.Serial(serial_port, baud_rate, timeout=1)

def move_arm(x, y, z):
    # Construct the command to move the arm
    command = f"X{x}Y{y}Z{z}\n"
    
    # Send the command to the serial port
    ser.write(command.encode())
    
    # Wait for a short moment to allow the arm to move
    time.sleep(1)

# Example usage:
if __name__ == "__main__":
    # Move the arm to position (100, 200, 50)
    move_arm(100, 200, 50)

    Reflection-- Even though we weren't able to finish this assignment before the deadline we were able to do a few things which were the coding and onshape designing
    


