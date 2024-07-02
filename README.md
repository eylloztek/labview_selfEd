# LabVIEW Lecture Notes

## Contents

- fahrenheit_to_celcius.vi: Converting Fahrenheit to Celcius with SubVI
- array_find.vi: Searching for a specific element in a 1D array
- write_to_csv.vi: transfering the informations of a person in a cluster to csv file
- serial_com_port.vi: send & receive message with serial COM port

## Details

### Fahrenheit to Celcius
In this training, a system that converts from Fahrenheit to Celsius using SubVI in LabVIEW was developed. SubVI is something similar to a subroutine in the text based languages. In LabVIEW, a SubVI (Sub-Virtual Instrument) is a subroutine or subVI that is used within another VI (Virtual Instrument), usually performing a specific task. SubVIs help make the LabVIEW program more modular and reduce complexity. SubVIs can be very useful when it is necessary to use the same functionality multiple times, especially in large projects. Once a SubVI is created, you can use that VI elsewhere and unify the complexity, resulting in a more understandable programming environment.

![SubVI example](https://github.com/eylloztek/labview_selfEd/blob/main/images/01.07.2024%20-%20create%20subVI.png)

### Searching Elements in a 1 Dimensional Array
In this training, a program was made to find a specific element in a one-dimensional array with random elements. We have an empty array with 20 elements. At each run, the array is filled with random elements. The element to be found is entered and it is checked whether it is in the array or not. For this, the "search 1D array" function in LabVIEW is used. Since the Search 1D array function works linearly, there is no need to sort the array. If the searched element is found, the loop ends and the result is shown. If the searched element is not found, the result is returned as -1.

![Search 1D array](https://github.com/eylloztek/labview_selfEd/blob/main/images/1D_array_search.png)

### Write the Informations to a CSV Spreadsheet
In this training, a program was created that converts the personal information in a cluster into csv format and writes it to a csv file. In LabVIEW, clusters are data structures that group multiple data elements of different types into a single unit. They are similar to structs in C. Clusters are used to organize related data together, making it easier to manage and pass complex data sets through the block diagram of a VI (Virtual Instrument).

First, a cluster is created where person information will be entered. If there are different types of data in the cluster (such as String and integer), conversion is done to these types to avoid errors. The path to this file is given so that the information from the cluster can be written to a csv file.

![write to csv file](https://github.com/eylloztek/labview_selfEd/blob/main/images/write_into_csv_spreadsheet.png)

### Serial Communication Ports 
In this training, a communication program was made using serial communication ports. Serial communication ports are used to transmit data one bit at a time over a single channel. They are essential for connecting devices and long-distance communication. Common examples include RS-232, USB, and Ethernet.

The front panel has two numeric inputs named x and y, which determine the numbers the program will use for calculations. After these inputs are summed, the result of x + y is displayed. Additionally, the user can select between two different COM ports, and the ports are operated through the Virtual Serial Ports Emulator. To display the result of the program's execution, there are "pass message" and "fail message" fields that show "Passed" or "Failed" messages. In the block diagram, the x and y inputs are connected for the summation process, and their sum is calculated. A comparison block checks if the sum is greater than 5. If the sum is not greater than 5 (False), the message "Good Luck!" is displayed; if the sum is greater than 5 (True), the message "Great!" is sent. "Error out 3" and "error out 4" are used to catch errors that may occur during serial communication. If the sum is greater than 5, a "Passed" message is shown; otherwise, a "Failed" message is displayed. Additionally, there is a stop button to terminate the program. After the user enters the values for x and y, the program calculates their sum. If the sum is greater than 5, the user-defined message (e.g., "Great!") is written in the "pass message" field. If the sum is less than or equal to 5, the message "Good Luck!" is written in the "fail message" field. At the end of the program, any errors are checked, and appropriate messages are displayed. This system uses serial communication to check whether a certain condition is met and shows the results to the user.

![serial COM port pass message](https://github.com/eylloztek/labview_selfEd/blob/main/images/send_receive_buffer_with_serialCOMport_passmessage.png)
![serial COM port fail message](https://github.com/eylloztek/labview_selfEd/blob/main/images/send_receive_buffer_with_serialCOMport_failmessage.png)
