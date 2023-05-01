Download Link: https://assignmentchef.com/product/solved-bicycle-parts-distributorship-java-program
<br>
5/5 - (5 votes)

You are a programmer working for Bicycle Parts Distributorship. BPD has a warehouse full of bicycle parts. The warehouse parts and database are as described in Project 1. In this increment of the project BPD has purchased vans and hired sales personnel who drive the vans. The sales personnel load their vans with bicycle parts, which they sell to bicycle shops located throughout the sales district. Each sales van is its own warehouse that has inventory. When a sales van is loaded with parts, the inventory in the main warehouse is decremented and the inventory in the sales van is incremented. Sometimes, a sales associate does not want to drive to the main warehouse to get a few parts. In these cases, sales associates agree to meet and move parts from one sales van warehouse to another.

Warehouse Parts Inventory Update

The warehouse parts inventory update shall be done by processing an inventory delivery file just like Project 1.

Sales Van Parts Inventory Update from Main Warehouse

When a sales associate visits the warehouse to load their van with parts, the sales associate arrives with a sales van delivery file that describes the bicycle parts that are to be moved from the main warehouse onto their van. The file consists of a sequence of comma-separated lines. The first line contains the name of the main warehouse followed by the name of a destination van, where parts are moved from the main warehouse to the destination. Each of the remaining lines contains the name of the bicycle part and the quantity that is to be moved from the main warehouse into the sales van warehouse. The following is an example.

mainWarehouse,salesVanC

WTB_saddle,4

26inTube,10

seatPost,2

Sales Van Parts Inventory Update from a Sales Van

When sales associate A meets with a sales associate B to get parts, sales associate A arrives with a sales van delivery file that describes the bicycle parts that are to be moved from sales associate B’s van into sales associate A’s van. The file consists of a sequence of comma-separated lines. The first line contains the name of the source van followed by the name of a destination van, where parts are moved from the source to the destination. Each of the remaining linescontains the name of the bicycle part and the quantity that is to be moved from the source van to the destination van. The following is an example.

salesVanA,salesVanB

WTB_saddle,4

26inTube,10

seatPost,2

carbonHandleBars42cm,25

When a sales van delivery file is processed in this case, the inventory in both the salesperson A’s delivery van warehouse and salesperson B’s delivery van warehouse are updated.

NOTE1: Read this specification carefully. You must implement the program as described.

NOTE2: The Bicycle Parts Distributorship project specifications use the term database as a general description of the underlying data that must be persistent across executions of your program. To satisfy the persistent requirement, your database will have to be a file (or files) that your program reads/writes. You do not have to create an SQL or NOSQL database.

Program Functional Requirements

Your program shall accomplish the following. NOTE: Requirements 1 through 9 are identical from Project 1; however, some implementation details such as filenames have been removed.

1. Your program shall have a warehouse database. The first time your program runs the warehouse database shall be empty or nonexistent.

2. Your program shall read the warehouse database upon starting. This shall establish the initial inventory in your internal data structures.

3. Your program shall write the internal data structures to the warehouse database upon exiting. The inventory in your internal data structures shall be saved such that upon running your program again, it starts with the same data as it ended with.

4. Your program shall read inventory delivery files (e.g., inventory.txt) as input by the user. Reading inventory delivery files updates the data in your internal data structures as follows.a) If the bicycle part is not a member of your internal data structure, the bicycle part is added.

b) If the bicycle part is is in your internal data structure, the list price is updated, the sales price is updated, the on sale indicator is updated, and the quantity is added to the current quantity on hand.

5. Your program shall show the bicycle part information by name.

6. Your program shall sell a bicycle part by part number from a warehouse. The sell shall allow the user to specify the warehouse. When a bicycle part is sold, you shall do the following for the specified warehouse.

a) Display the part name, the part cost, which will be either the list price of sale price.

b) Display the time the part was sold.

c) Decrement the quantity.

7. Your program shall allow a new part to be entered interactively.

8. Your program shall display all parts in alphabetical order. This display shall show all inventory attributes (name, number, list price, sale price, on-sale indicator, quantity). The display alphabetical order shall allow specifying a particular warehouse as follows.

a) The total collection of warehouses

b) The main warehouse

c) Each individual sales van warehouse

9. Your program shall display all parts in part number order. This display shall show all inventory attributes (name, number, list price, sale price, on-sale indicator, quantity). The display part number order shall allow specifying a particular warehouse as follows.

a) The total collection of warehouses

b) The main warehouse

c) Each individual sales van warehouse

10. Your program shall allow the user to add a sales van to the fleet.

11. Your program shall allow a sales associate to move inventory from the main warehouse into the sales van warehouse.

12. Your program shall allow a sales associate to move inventory from another sales van warehouse into its sales van warehouse.

Object-oriented Requirements

1. Your program shall define and use a Java Interface as part of its solution.

2. Your program shall define and use inheritance as part of its solution.

User Interface Requirements

1. Your program shall have a JavaFX Graphical User Interface. The layout of the GUI

panels is your design, but I recommend you create a simple interface.