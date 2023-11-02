# CS1120
Python 
CS/CYCS1120 (Python) –Fall 2023
Programming Project #3
Project Overview
Project Objectives
•
•
•
Reviewing OOP
Reviewing Inheritance
Reviewing File I/O
A store has classified type of cars it is selling as either an imported car or a domestic car. Your
program should have one superclass called ‘Car’ and two other derived classes: ‘ImportCar’ and
‘DomesticCar’. The super class Car keeps the common information like: Brand, Model, Year,
Type, and Price.
Two sub classes – ImportCar class and DomesticCar class – must extend the super class Car to
save and retrieve general information. In the ImportCar subclass two new data attributes
Country and Tax are added to keep information about the export country and importTax (%) of
this car. In the DomesticCar class the new data attribute State is added to store the state where
the car was produced. No additional tax is levied on domestic cars. All data field’s accessibility
is ‘private’. Define and use the accessor methods to access the private members. The super
class is realized by sub classes, when they are created and call the super class,__init() method
as a part of their initializations.
__Brand
__Model
__Year
__Price
__Type
get_brand()
set_brand()
get_model()
set_model()
get_year()
set_year()
get_price()
set_price()
get_type()
set_type()
print_info()
__State
get_state()
set_state()
print_info()
__Country
__Tax
get_country()
set_country()
get_tax()
set_tax()
print_info()
ImportCar
DomesticCar
Number of imported cars = 3
Number of domestic cars = 5
Total = 8
2
“D” indicates a domestic car, and you have to use a DomesticCar object to store its information.
“I” indicates an imported car, and you have to use an ImportCar object.
Output would be a listing of cars in the carsCatagoryWise.txt file and console as follows:
Read all car information from the input file (carsInStock.txt) and save it to the correct type of
object. In the input file each line will start with either ‘I’ or ‘D’ to indicate the classification of
the car. You should use lists to save the information about the current collection of cars.
Example of 2 lines in the carsInStock.txt and carsExpectedToArrive.txt files are:
Project Structure
First Step:
D Ford F150 2002 17000 Truck MI
I Toyota Camry 2004 20000 Sedan Japan 10
Imported Cars:
Toyota Camry 2014 20,000.00 Sedan Japan 10% BMW 325i 2013 30,000.00
Sedan Germany 8% Toyota LexusRX30 2015 42,000.00 Sedan Japan 10%
Domestic Cars:
Ford F150 2012 17,000.00 Truck MI
Chrysler Pacifica 2013 18,000.00 Sedan TX
Chevrolet TahoeLS 2010 7,000.00 Coup TX
Chevrolet Silverado 2011 10,000.00 Van MI
Ford Econoline 2012 16,000.00 Sedan MI
Again, print the new list of cars as in Step 1.
Note: Make sure that you are using polymorphism to call the
appropriate
The print_info() method in the subclasses should be redefined to override the
in the superclass.
Add the new cars from the input in carsExpectedToArrive.txt file to the existing list. For
example, cars expected to arrive may be
method.
method
For all domestic cars increase their base price by adding 15% to each of them. Since the car
market seems to be flooded with Japanese cars, Govt XYZ levies an additional import tax of
5% for cars imported from Japan, so update their tax by adding 5%. In order to do this you
MUST create methods in the corresponding classes. Print the list of these cars again with the
final pricing and the possibly increased import tax as done in Step 1.
Third Step:
Second Step:
I Toyota Avalon 2012 14000 Sedan Japan 10
D Ford Mustang 2010 19000 Sedan MI
I Honda AccordEX 2013 12500 Coup Japan 5
print_info()
print_info()
3
Imported Cars
Toyota Camry 2014 20,000.00 Sedan Japan 15% BMW 325i 2013 30,000.00 Sedan
Germany 8% Toyota LexusRX30 2015 42,000.00 Sedan Japan 15% Toyota Avalon 2012
14,000.00 Sedan Japan 12% Honda AccordEX 2013 12,500.00 Coup Japan 12%
Domestic Cars
Ford F150 2012 19,550.00 Truck MI
Chrysler Pacifica 2013 20,700.00 Sedan TX
Chevrolet TahoeLS 2010 8,050.00 Coup TX
Chevrolet Silverado 2011 11,500.00 Van MI
Ford Econoline 2012 18,400.00 Sedan MI
Ford Mustang 2010 11,500.00 Sedan MI
Number of imported cars = 5
Number of domestic cars = 6
Total = 11
NOTE
Fouth Step:
Design Requirements
Note that the price total includes the sales tax of 6% and an import tax, if
any. Deliverables
print the list of all cars in the store whose price is less than or equal to $15000. Make sure that
your list’s format matches the example below and ordered by price: low to high:
Submit a .zip file that contains all your files (CS1120_Proj04_LastName.zip), including:
o Program files
o I/O files
Provides this information in every file in your project:
: You may submit beyond the due date but your submission date/time will be recorded.
The penalty for late submissions as stated in the course syllabus will be applied in grading any
assignment submitted late.
You MUST use Inheritance and polymorphism for this project. Your program should have one
superclass called ‘Car’ and two other subclasses: ‘ImportCar’ and ‘DomesticCar’, which
includes the attributes, methods for filling, updating and printing them.
You should have a separate class containing your main() method, which is the tester of your
project.
Filter price less than: 15000.0
Toyota Avalon 2012 14,000.00 Sedan Japan 12% Honda AccordEX 2013
12,500.00 Coup Japan 12% Chevrolet Silverado 2011 11,500.00 Van MI
Ford Mustang 2010 11,500.00 Sedan MI
Chevrolet TahoeLS 2010 8,050.00 Coup TX
Number of cars = 5
Total price of cars in the Stock: $236,464.80
•
•
# Project No.:
# Author:
# Description:
5
Design Hints
Additional Requirements
See a sample report below. Use the EXACT format/wording/spacing/labeling/… shown in
sample. (use EXACT format – and NO HARDCODING of the data itself)
You may want to use two lists to save car’s information. Also, it is possible to have two counters
to keep the total number of imported cars and total number of domestic cars loaded.
Coding Standards: You must adhere to all conventions applicable to writing programs. This includes
the use of white spaces and indentations for readability, the use of comments to explain the meaning of
various methods and attributes, and the conventions for naming classes, variables, method parameters
and methods.
Example Output
File - CarTester
Page 1 of 2
Welcome to Domestic/Imported Cars Application
Step One:
Please enter a file name (with information about Cars in Stock):
carsInStock.txt Input file name for Cars in Stock: carsInStock.txt
Imported Cars
ToyotaCamry2014 20,000.00 Sedan Japan10%
BMW325i2013 30,000.00 Sedan Germany8%
ToyotaLexusRX30 2015 42,000.00 Sedan Japan10%
Domestic Cars
FordF1502012 17,000.00 Truck MI
Chrysler Pacifica 2013 18,000.00 Sedan TX
Chevrolet TahoeLS 2010 7,000.00 Coup TX
Chevrolet Silverado 2011 10,000.00 Van MI
FordEconoline 2012 16,000.00 Sedan MI
Number of imported cars = 3
Number of domestic cars = 5
Total = 8
Step Two
Please enter a file name (with information about Cars expected to arrive):
carsExpectedToArrive.txt Input file name for Cars expected to arrive:
carsExpectedToArrive.txt
Imported Cars
ToyotaCamry2014 20,000.00 Sedan Japan10%
BMW325i2013 30,000.00 Sedan Germany8%
ToyotaLexusRX30 2015 42,000.00 Sedan Japan10%
ToyotaAvalon2012 14,000.00 Sedan Japan7%
HondaAccordEX 2013 12,500.00 Coup Japan7%
Domestic Cars
FordF1502012 17,000.00 Truck MI
Chrysler Pacifica 2013 18,000.00 Sedan TX
Chevrolet TahoeLS 2010 7,000.00 Coup TX
Chevrolet Silverado 2011 10,000.00 Van MI
FordEconoline 2012 16,000.00 Sedan MI
FordMustang 2010 10,000.00 Sedan MI
Number of imported cars = 5
Number of domestic cars = 6
Total = 11
Step Three
Imported Cars
ToyotaCamry2014 20,000.00 Sedan Japan15%
BMW325i2013 30,000.00 Sedan Germany8%
ToyotaLexusRX30 2015 42,000.00 Sedan Japan15%
ToyotaAvalon2012 14,000.00 Sedan Japan12%
HondaAccordEX 2013 12,500.00 Coup Japan12%
Domestic Cars
FordF1502012 19,550.00 Truck MI
Chrysler Pacifica 2013 20,700.00 Sedan TX
File - CarTester
Page 2 of 2
Chevrolet TahoeLS 2010 8,050.00 Coup TX
Chevrolet Silverado 2011 11,500.00 Van MI
Ford Econoline 2012 18,400.00 Sedan MI
Ford Mustang 2010 11,500.00 Sedan MI
Number of imported cars = 5
Number of domestic cars = 6
Total = 11
Filter price less than: 15000.0
Chevrolet TahoeLS 2010 8,050.00 Coup TX
Chevrolet Silverado 2011 11,500.00 Van MI
Ford Mustang 2010 11,500.00 Sedan MI
Honda AccordEX 2013 12,500.00 Coup Japan 12% Toyota Avalon 2012
14,000.00 Sedan Japan 12%
Number of cars = 5
Total price of cars in the Stock: $236,464.80
Process finished with exit code 0
