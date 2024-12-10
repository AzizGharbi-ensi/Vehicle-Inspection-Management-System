This project implements a Vehicle Inspection Management System in C. It uses various programming techniques like file handling, dynamic memory allocation, pointers, linked lists, stacks, and queues to simulate the process of organizing vehicle inspections.
 Here's a detailed explanation of each part:

1. Header File (inspection_system.h)
This file declares the data structures and function prototypes used in the project.

Key Data Structures
Vehicle:

Represents a vehicle in the system with attributes:
licensePlate: Vehicle's license plate number.
ownerName: Owner's name.
model: Vehicle model.
year: Year of manufacture.
next: Pointer to the next vehicle in the linked list.
StackNode:

Represents a single node in a stack used for scheduling inspections in LIFO (Last In, First Out) order.
Stores:
licensePlate: License plate of the vehicle.
next: Pointer to the next stack node.
QueueNode and Queue:

Used for scheduling inspections in FIFO (First In, First Out) order.
QueueNode:
Stores licensePlate and a pointer to the next node.
Queue:
Contains pointers to the front and rear of the queue.
2. Implementation File (inspection_system.c)
This file implements the functions declared in the header file. Here's what each function does:

Vehicle Management
addVehicle:

Dynamically creates a new Vehicle node and adds it to the linked list.
Returns the updated list's head.
displayVehicles:

Traverses the linked list and prints all vehicle details.
If the list is empty, it displays an appropriate message.
saveToFile:

Saves all vehicles in the linked list to a file in a readable format.
Useful for persisting data between program runs.
loadFromFile:

Reads vehicle data from a file and reconstructs the linked list.
Dynamically allocates memory for each node.
Scheduling and Processing Inspections
scheduleInspectionLIFO:

Adds a vehicle to the top of a stack (LIFO).
Dynamically allocates memory for a new stack node.
processInspectionLIFO:

Removes and processes the vehicle at the top of the stack.
scheduleInspectionFIFO:

Adds a vehicle to the rear of a queue (FIFO).
Dynamically allocates memory for a new queue node.
processInspectionFIFO:

Removes and processes the vehicle at the front of the queue.
3. Main File (main.c)
This file is the entry point of the program. It handles user interaction through a menu-driven interface.

Menu Options
Add Vehicle:

Prompts the user to enter vehicle details.
Adds the vehicle to the linked list.
Display Vehicles:

Displays all vehicles currently stored in the system.
Save Vehicles to File:

Saves all vehicle data to a file named vehicles.txt.
Load Vehicles from File:

Loads vehicle data from vehicles.txt into memory.
Schedule Inspection (LIFO):

Adds a vehicle to the inspection stack using LIFO order.
Process Inspection (LIFO):

Processes the top vehicle from the inspection stack.
Schedule Inspection (FIFO):

Adds a vehicle to the inspection queue using FIFO order.
Process Inspection (FIFO):

Processes the front vehicle from the inspection queue.
Exit:

Exits the program.
How It Works
The program starts by displaying a menu.
Users can add vehicles, schedule inspections, or save/load data to/from a file.
Inspections can be organized in two ways:
LIFO: Vehicles are inspected in reverse order of scheduling.
FIFO: Vehicles are inspected in the order they were scheduled.
The program uses:
Dynamic memory allocation for creating nodes (vehicles, stack, queue).
File handling for saving/loading vehicle data.
Pointers to manage linked lists, stacks, and queues.
Example Usage
Adding and Saving Vehicles
Add a vehicle:
License Plate: 129tu3093
Owner: Ahmed Aziz Gharbi
Model: Clio 2
Year: 2006
Save to vehicles.txt.
Scheduling Inspections
Schedule 129tu3093 for inspection using both LIFO and FIFO.
Processing the LIFO stack will inspect 129tu3093 first.
Processing the FIFO queue will inspect vehicles in order of addition.
This modular design allows you to manage a vehicle inspection system efficiently, demonstrating concepts like data structures, file I/O, and memory management.
