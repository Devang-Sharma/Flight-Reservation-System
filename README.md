# Flight-Reservation-System
This flight reservation system project works on 6 key features, to book domestic flights, to book international flights(of two types, Local to International and International to International), To access info. about all the tickets booked in the program using an access code, To cancel a booked ticket by giving the ticket no. and reference no. and finally to print the ticket details

Now, here is the technical description of this project explaining the various classes and functions involved in the making.

Classes used-
	“Search” – Class to show Available Boarding Locations, Destination and Routes.
  	Member-Functions: -
   1.	L2I(void): -
      	Return type void.
      	Prints Local to International Flight routes.
   2.	internsearch(void): -
      	Return type void.
      	Prints International to International Flight routes.
  3.	localsearch(void): -
      	Return type void.
      	Prints Local to Local Flight routes.
      	“payment” - Class to calculate Flight Bill.	
	“main1” - Class main1 is Mother of all Classes and Functions.
    	Member-Functions: -
    1.	getdata(void):- main1::getdata() Provides User-Interface to access all Functionalities of the Program.
      	Return type void.
      	Provides following choices:
          o	To book local to local flight.
          o	To book local to international or international to international flight.
          o	To Search for Flights.
          o	To check logs.
          o	To Cancel Ticket.
          o	To Print Personal Ticket.
          o	To Exit Program
	“local”- Class local inherits booking Class and redefines getdata() to book tickets for Local To Local Routes
    	Member-Functions: -
    1.	getdata(void): -
      	Return type void.
      	Asks user for Airline, Class(Business, Economy).
      	Calls mytime::getdata()
      	Calls booking::getdata(int)
      	Calls booking::show(int)
      	“international”- Class international inherits booking Class and redefines getdata() to book tickets for Local To International & International To International Routes
      	Member-Functions: -
	“booking”- Class booking inherits passenger publicly and defines getdata() and show() to take input() for personal info and print Ticket respectively.
    	Member-Functions: -
    1.	getdata(int): -
      	Asks user for:
          o	First name
          o	Last name
          o	Address 
          o	Passport No.
          o	Phone No.
          o	Gmail
          o	Boarding Location
          o	Destination
          o	Flight Date
        Return type void.
    2.	show(void): - 
      	Return type void.
      	Write Passenger class instance in Data File.
      	Shows the ticket on screen.
      	Generates and print Ticket no. and Reference no.

	“passenger” – It stores Users' Personal Information and Ticket Details
    	Member-Functions: -
    1.	show_logs(void): -
        	Prints single ticket.
        	Return type void.
    2.	getdata(void): -Virtual Function to be defined in sub-class.
    3.	show(void): -Virtual Function to be defined in sub-class.
	“mytime” – 
    	Member-Functions: -
    1.	getdata(void): -
      	Asks User for flight time.
      	Return type void.
    2.	show(void): -
      	Displays Flight time on screen.
      	Return type void.
	“payment” - Class to calculate Flight Bill.	
    	Member-Functions:-
    1.	Calc_Bill(char [],char[],char[]): -
      	Return type void.
      	calculates amount of ticket with the help of Boarding location, Destination and Class(Business/Economy).
    2.	waystopay(void): -
      	Return type void.
      	Provides interface to ask user to pay via UPI or Bank Transfer.
    3.	Pay_UPI(void): -
      	Asks user for Mobile no.
      	Verify Payment through OTP and CAPTCHA Verification. 

    4.	Pay_Bank(void): -
      	Asks user for Bank acc. no., acc. name, IFSC Code and IPIN.

	Member-Functions:-
1.	Calc_Bill(char [],char[],char[]): -
	Return type void.
	calculates amount of ticket with the help of Boarding location, Destination and Class(Business/Economy).
2.	waystopay(void): -
	Return type void.
	Provides interface to ask user to pay via UPI or Bank Transfer.
3.	Pay_UPI(void): -
	Asks user for Mobile no.
	Verify Payment through OTP and CAPTCHA Verification. 

4.	Pay_Bank(void): -
	Asks user for Bank acc. no., acc. name, IFSC Code and IPIN.
	“mytime” – 
	Member-Functions: -
1.	getdata(void): -
	Asks User for flight time.
	Return type void.
2.	show(void): -
	Displays Flight time on screen.
	Return type void.
	“passenger” – It stores Users' Personal Information and Ticket Details
	Member-Functions: -
1.	show_logs(void): -
	Prints single ticket.
	Return type void.
2.	getdata(void): -Virtual Function to be defined in sub-class.
3.	show(void): -Virtual Function to be defined in sub-class.
	“booking”- Class booking inherits passenger publicly and defines getdata() and show() to take input() for personal info and print Ticket respectively.
	Member-Functions: -
1.	getdata(int): -
	Asks user for:
o	First name
o	Last name
o	Address 
o	Passport No.
o	Phone No.
o	Gmail
o	Boarding Location
o	Destination
o	Flight Date
	Return type void.
2.	show(void): - 
	Return type void.
	Write Passenger class instance in Data File.
	Shows the ticket on screen.
	Generates and print Ticket no. and Reference no.
	“local”- Class local inherits booking Class and redefines getdata() to book tickets for Local To Local Routes
	Member-Functions: -
1.	getdata(void): -
	Return type void.
	Asks user for Airline, Class(Business, Economy).
	Calls mytime::getdata()
	Calls booking::getdata(int)
	Calls booking::show(int)
	“international”- Class international inherits booking Class and redefines getdata() to book tickets for Local To International & International To International Routes
	Member-Functions: -
1.	getdata(void): -
	Return type void.
	Asks user for Airline, Class(Business, Economy).
	Calls mytime::getdata()
	Calls booking::getdata(int)
	Calls booking::show(int)

	“main1” - Class main1 is Mother of all Classes and Functions.
	Member-Functions: -
1.	getdata(void):- main1::getdata() Provides User-Interface to access all Functionalities of the Program.
	Return type void.
	Provides following choices:
o	To book local to local flight.
o	To book local to international or international to international flight.
o	To Search for Flights.
o	To check logs.
o	To Cancel Ticket.
o	To Print Personal Ticket.
o	To Exit Program.
Functions used-
	checkCaptcha(string &captcha, string &user_captcha)
•	return 1 if Captcha entered by user is equal to Captcha generated by generateCaptcha().
•	return 0 if Captcha entered by user is not equal to Captcha generated by generateCaptcha().
	generateCaptcha(void)
•	returns Captcha string generated using <ctime.h>,random function and push_back function.
	captcha_validation(void)
•	Return type void.
•	Calls generateCaptcha() and checkCaptcha() to generate and validate Captcha.
•	Terminates program if Captcha is entered wrongly thrice.
	otp_validation(void)
•	Return type void.
•	Generates OTP and validates it.
•	Terminates Program if user enters wrong OTP thrice.
