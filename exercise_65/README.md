# Arrey's Dealership

## Summary
Your reputation for building command line apps is growing. Fran's orange grove is blooming and Arnie's Bistro is booming.

Arnie's friend Arrey has a small used car dealership.  She is about to receive a big shipment of used cars from Japan and he wants an application to help her manage her growing inventory.  It just so happens that the same programmer who left Arnie's project half-done, did the same with Arrey's.  It's your job to ship the product that Arrey wants before the shipment of cars arrives.


### Inventory Management System Use Cases:
Arrey wants a quick way to get an overview of her cars.  She wants to be able to (1) list all the cars in his inventory and (2) list specific subsets of cars: cars of a given make (e.g., Honda), cars made before a given year, and cars made after a given year.


## Releases
### Part 0: Review the Code Base
As mentioned in the Summary, the previous developer left some code. Review the provided code. How was the developer approaching the problem? Does this approach make sense? Are there things you would do differently? Are there things you would keep?


### Part 1 : Implement the Minimum Viable Product
Building on the provided code base, implement the use cases described in the Summary. Remember, Arrey wants a working application before his shipment arrives, so we need to focus on just these features.

To recap how the program works, when users want to list all cars, the program should display something like Figure 1.  When users want to see a subset of cars (e.g., cars of a certain make), the program should display something like Figure 2.


```
$ ruby inventory_management.rb list
2001 Honda Accord (55839)
2004 Toyota Corolla (98773)
2002 Peugeot 307 (66761)
2003 BMW M5 (10029)
2002 Honda Civic (00822)
2012 Toyota Prius (78990)
1971 Daihatsu Hijet (38384)
```
*Figure 1*.  Listing all the cars

```
$ ruby inventory_management.rb search make toyota
2004 Toyota Corolla (98773)
2012 Toyota Prius (78990)

$ ruby inventory_management.rb search pre 2000
1971 Daihatsu Hijet (38384)

$ ruby inventory_management.rb search post 2009
2010 Honda Civic (00822)
2012 Toyota Prius (78990)
```
*Figure 2*.  Displaying subsets of cars.


### Part 2: Update Inventory
Currently, Arrey is able to view his inventory through this application.  But, when Arrey acquires or sells a car, he has to update his inventory by editing the text file where his inventory data is held.  Arrey would like to update the text file through this application.  Update the application so that Arrey can add or remove cars from the text file (see Figures 3 and 4).

```
$ ruby inventory_management.rb remove 55839
```
*Figure 3*.  Removing a car by specifying an inventory id.


```
$ ruby inventory_management.rb add 98374 1995 Mazda 626
```
*Figure 4.*  Adding a car, specifying an inventory id, year, make, and model.

