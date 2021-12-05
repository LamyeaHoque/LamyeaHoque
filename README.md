- 👋 Hi, I’m @LamyeaHoque
- 👀 I’m interested in software engineering....
- 🌱 I’m currently learning Java...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
LamyeaHoque/LamyeaHoque is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
//HW#1 print 4 digit
import java.util.Scanner;
public class Fourdigit {
public static void main(String args[]) {
Scanner keyboard = new Scanner(System.in);
System.out.print("Enter a 4-digit number ");
int n;
n=keyboard.nextInt();
System.out.println(n/1000);
n=n%1000;
System.out.println(n/100);
n=n%100;
System.out.println(n/10);
n=n%10;
System.out.println(n/1);
}
}
//HW#2
import java.util.Scanner;
public class GradesGraph {
	
	private int Acount;
	private int Bcount;
	private int Ccount;
	private int Dcount;
	private int Fcount;
	private int astrskCount;

	
	public void readInput() {
	Scanner keyboard = new Scanner(System.in);

	System.out.println("How many A's?");
	Acount = keyboard.nextInt();
	
	System.out.println("How many B's?");
	Bcount = keyboard.nextInt();
	
	System.out.println("How many C's?");
	Ccount = keyboard.nextInt();
	
	System.out.println("How many D's?");
	Dcount = keyboard.nextInt();
	
	System.out.println("How many F's?");
	Fcount = keyboard.nextInt();
	
	}
	
	public void writeOutput() {
		System.out.println("Number of A's = " + Acount);
		System.out.println("Number of B's = " + Bcount);
		System.out.println("Number of C's = " + Ccount);
		System.out.println("Number of D's = " + Dcount);
		System.out.println("Number of F's = " + Fcount);
		}

	
	
public void set(int newAcount, int newBcount,int newCcount, 
		int newDcount,int newFcount) {

	Acount = newAcount;
	Bcount = newBcount;
	Ccount = newCcount;
	Dcount = newDcount;
	Fcount = newFcount;
	}

public void writeAcount() {
	System.out.println("Number of A's = " + Acount);
	}

	public void writeBcount() {
	System.out.println("Number of B's = " + Bcount);
	}

	public void writeCcount() {
	System.out.println("Number of C's = " + Ccount);
	}

	public void writeDcount() {
	System.out.println("Number of D's = " + Dcount);
	}

	public void writeFcount() {
	System.out.println("Number of F's = " + Fcount);
	}


	public int getAcount() {
	return Acount;
	}

	public int getBcount() {
	return Bcount;
	}

	public int getCcount() {
	return Ccount;
	}

	public int getDcount() {
	return Dcount;
	}

	public int getFcount() {
	return Fcount;
	}

	//these setters will set individual grades to newGradeCount
	public void setAcount(int newAcount) {
	Acount = newAcount;
	}

	public void setBcount(int newBcount) {
	Bcount = newBcount;
	}

	public void setCcount(int newCcount) {
	Ccount = newCcount;
	}

	public void setDcount(int newDcount) {
	Dcount = newDcount;
	}

	public void setFcount(int newFcount) {
	Fcount = newFcount;
	}

	
	

	public int getTotalNumberOfGrades() { 
	return (Acount + Bcount + Ccount + Dcount + Fcount);
	}

	//These method will get the percentages
	public int getPercentA() {
	return (int)((float)Acount/this.getTotalNumberOfGrades() * 100
	+ 0.5);
	}

	public int getPercentB() {
	return (int)((float)Bcount/this.getTotalNumberOfGrades() * 100
	+ 0.5);
	}

	public int getPercentC() {
	return (int)((float)Ccount/this.getTotalNumberOfGrades() * 100
	+ 0.5);
	}

	public int getPercentD() {
	return (int)((float)Dcount/this.getTotalNumberOfGrades() * 100
	+ 0.5);
	}

	public int getPercentF() {
	return (int)((float)Fcount/this.getTotalNumberOfGrades() * 100
	+ 0.5);
	}


	public void draw() { 
	//this line for Drawing scale
	System.out.println("2  10  20  30  40  50  60  70  80  90  100");
	System.out.println("|   |   |   |   |   |   |   |   |   |   |");
	System.out.println("********************************************");

	//this "For loops" will count the asterisks 

	for(astrskCount = 1;
	astrskCount <= getPercentA()/2;
	astrskCount++) {
	System.out.print("*");
	}
	System.out.println(" A");

	for(astrskCount = 1;
	astrskCount <= getPercentB()/2;
	astrskCount++) {
	System.out.print("*");
	}
	System.out.println(" B");

	for(astrskCount = 1;
	astrskCount <= getPercentC()/2;
	astrskCount++) {
	System.out.print("*");
	}
	System.out.println(" C");

	for(astrskCount = 1;
	astrskCount <= getPercentD()/2;
	astrskCount++) {
	System.out.print("*");
	}
	System.out.println(" D");

	for(astrskCount = 1;
	astrskCount <= getPercentF()/2;
	astrskCount++) {
	System.out.print("*");
	}
	System.out.println(" F");
	}
} 

//HW#4 ---Asterik diamond

import java.util.Scanner;
public class Diamond {
public static void main(String[] args) {
Scanner keyboard = new Scanner(System.in);
System.out.println("Enter value for diamond side:");
int size = keyboard.nextInt();
keyboard.close();
System.out.println();
// that loop will print the top of half of the diamond
for(int i=0;i<size+1;i++) {
for(int j=size+1;j>i;j--) {
System.out.print('*');
}
for(int j=0;j<i;j++) {
System.out.print(' ');
System.out.print(' ');
}
// This for loop will print asterisk for second half of the line
for(int j=size+1;j>i;j--) {
System.out.print('*');
}
System.out.println(); // that will print new line
}
// this for loop will print the bottom half of the diamond
for(int i=size-1;i>=0;i--) {
for(int j=size+1;j>i;j--) {
System.out.print('*');
}
// this will print blank space for the line of the diamond
for(int j=0;j<i;j++) {
System.out.print(' ');
System.out.print(' ');
}
// and that will print asterisk for the last half of line of the diamond
for(int j=size+1;j>i;j--) {
System.out.print('*');
}
System.out.println(); // print new line
}
}


//HW#5 
//This program will work for the attached TemperatureTest.java
import java.util.Scanner;
public class Temperature{
private double temperature;
private char scale;
//Four constructors are bellow
public Temperature(double temperature)//Default constructor
{
this.temperature = temperature;
this.scale = 'c';
}
public Temperature(char scale) // Constructor for number of scale
{
this.temperature = (double)0.0;
this.scale = scale;}
//one constructor for both the degree and scale
public Temperature(double temperature, char scale){
this.temperature = temperature;
this.scale = scale;
}
public Temperature() //constructor for number of degrees
{
this.temperature = (double)0.0;
this.scale = 'c';
}
//Two accessor methods
//This is to return the temperature in degrees Celsius
public double getC(){
if(this.scale == 'c' |
| this.scale == 'C')
return this.temperature;
else
return ((this.temperature - 32) / 1.8);
}
//This is to return the temperature in degrees Fahrenheit
public double getF(){
if(this.scale == 'f' |
| this.scale == 'F')
return this.temperature;
else
return ((this.temperature*1.8) + 32);
}
//Three set method is bellow
//This set method is to set the number of degrees
public void set(double temperature)
{
this.temperature = temperature;
}
//this set method is to set the number of scale
public void set(char scale){
this.scale = scale;
}
//this set method is to set the number of degree and scale
public void set(double temperature, char scale){
this.temperature = temperature;
this.scale = scale;
}
//Three comparison method:
//This is the equal method
public boolean equals(Temperature other){
return this.getC() == other.getC();
}
//this will calculate the LessThan method
public boolean isLessThan(Temperature other){
return this.getC() < other.getC();
}
//This will calculate the GreaterThan method
public boolean isGreaterThan(Temperature other){
return this.getC() > other.getC();
}
// write output
public void writeOutput(){
System.out.println(this.temperature+" degrees "+this.scale);
}
// this will read the input
public void readInput(){
Scanner input = new Scanner(System.in);
System.out.println("Please enter a Temperature: ");
double t = input.nextDouble();
System.out.println("Scale?(c for celsius/f for fahrenheit): ");
char s = input.next().charAt(0);
this.set(t, s);
}
public void writeC(){
System.out.println(this.getC()+" degrees c");
}
public void writeF(){
System.out.println(this.getF()+" degrees f");
}
}

HW#6
//This Java program will allow students to schedule appointments
import java.util.*;
import java.util.Scanner;
public class Schedule {
public static void main(String[] args) {
Scanner in = new Scanner(System.in);
//index of the array is the time slot
int all_full=0;
String arr[]=new String[6];
System.out.println("Welcome to the Appointment Scheduler");
System.out.println("You can schudule an appointment at 1,2,3,4,5,6 PM.");
// Running the loop till all the slots are full
while(all_full==0)
{
// the try block
try
{
// Asking for name input
System.out.println("What is your name?");
String name=in.nextLine();
// Asking for preferred input
System.out.println("When would you like the appointment?");
int time_slot=in.nextInt();
in.nextLine();
// Checking if the time slot entered by user is valid or not
if(time_slot<1 |
| time_slot>6)
{
// If the time slot is not valid then we throw the exception InvalidTimeException
throw new InvalidTimeException();
}
// An empty time slot will have null as its value
else if(arr[time_slot-1]!=null)
{
// If the time slot is not empty then we throw the exception TimeInUseException
throw new TimeInUseException();
}
// If the time slot is valid and also empty we then fill the time slot with the name
else
{
// Assigning the time slot with the user name
arr[time_slot-1]=name;
}
}
// catch block for the InvalidTimeException
catch(InvalidTimeException itex)
{
System.out.println("Sorry!! The time you entered is invalid.\n Please enter again.\
n");
}
// catch block for TimeInUseException
catch(TimeInUseException tiuex)
{
System.out.println("Sorry!!The time you entered is already booked.\n Please enter
again.\n");
}
int count=0;
for(int i=0;i<6;i++)
{
// Checking if the slot is full
if(arr[i]!=null)
{
// If the slot is full, we increase the count
count++;
}
}
// After checking all the slots we check if the count is 6
if(count==6)
{
// If count is 6 then we set the variable all_full to 1
all_full=1;
}
}
System.out.println();
System.out.println("Scheduled Appointments:");
System.out.println("All the Appointments made");
for(int i=0; i<6; i++) {
System.out.println("At "+(i+1)+"PM is "+arr[i]);
}
System.out.println();
}
}
//Invalidtime exception
class InvalidTimeException extends Exception{
private String msg;
InvalidTimeException(){
msg = "The Time Slot entered is not valid";//default message
}
//parameterized constructor
public InvalidTimeException(String msg) {
super(msg);//for getMessage()
this.msg = msg;//custom message
}
}
//Inuse time exception
class TimeInUseException extends Exception{
private String msg;
TimeInUseException(){
msg = "This time slot is already taken";//default message
}
//parameterized constructor
public TimeInUseException(String msg) {
super(msg);//for getMessage()
this.msg = msg;//custom message
}
}


//Data Structure
HW#1
//bank.java 
//demonstrates basic OOP syntax 
//to run this program: C>java BankApp //////////////////////////////////////////////////////////////// 

public class BankAccount 
{
	   private double balance; // account balance

	   public BankAccount(double openingBalance) // constructor

	   {
	       balance = openingBalance;
	   }

	   public void deposit(double amount) // for making deposit
	   {
	       if (balance > 0)
	           balance = balance + amount;
	      else
	           System.out.println("Sorry!! you can't deposit negative amount");
	   }

	   public void withdraw(double amount) //  makes withdrawal

	   {
	       if (balance >= amount)
	           balance = balance - amount;
	      else
	          System.out.println("ERROR!! Insufficient funds");

	   }

	   public void display() // displays balance

	   {
	       System.out.println("balance=" + balance);
	   }
}

//	} // end class BankAccount
public class BankApp {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		BankAccount ba1 = new BankAccount(100.00); // create account

	       System.out.print("Before transactions, ");

	       ba1.display(); // display balance

	       ba1.deposit(74.35); // make deposit

	       ba1.withdraw(20.00); // make withdrawal

	       System.out.print("After transactions, ");

	       ba1.display(); // display balance
	       ba1.withdraw(1500);	       
	   } // end main()



	}

//HW#2

		// array in sorted order, from max at 0 to min at size-1
		private int maxSize;
		private long[] queArray;
		private int nItems;
		//-------------------------------------------------------------
		public PriorityQ(int s) // constructor
		{
		maxSize = s;
		queArray = new long[maxSize];
		nItems = 0;
		}
		//-------------------------------------------------------------
		public void insert(long item) // insert item
		{
		int j;
		if(nItems==0) // if no items,
		queArray[nItems++] = item; // insert at 0
		else // if items,
		{
		for(j=nItems-1; j>=0; j--) // start at end,
		{
		if( item > queArray[j] ) // if new item larger,
		queArray[j+1] = queArray[j]; // shift upward
		
		else // if smaller,
		break; // done shifting
		} // end for
		queArray[j+1] = item; // insert it
		nItems++;
		} // end else (nItems > 0)
		} // end insert()
		//-------------------------------------------------------------
		public long remove() // remove minimum item
		{ int indxmin=0;
		for (int i=1; i<nItems; i++) {
			if(queArray[i] < queArray[indxmin]) {
				indxmin=i;
			}
		}
		long elem = queArray[indxmin];
		for( int i= indxmin; i< nItems-1; i++ ) {
			queArray[i]= queArray[i+1];
		}
		nItems--;
			//return queArray[--nItems];
		return elem;
		}
		//-------------------------------------------------------------
		public long peekMin() // peek at minimum item
		{ return queArray[nItems-1]; }
		//-------------------------------------------------------------
		public boolean isEmpty() // true if queue is empty
		{ return (nItems==0); }
		//-------------------------------------------------------------
		public boolean isFull() // true if queue is full
		{ return (nItems == maxSize); }
		//-------------------------------------------------------------
		//----------------------------------------------------------
		public void display() {
			System.out.print("Queue: ");
			for (int i=0; i < nItems; i++) {
				System.out.print(queArray[i]);
				if(i!= nItems -1) {
					System.out.print(" , ");
				}
			}
			if(nItems==0)//this is to check whether the queue is empty or not
			{
				System.out.println("There are no element left in queue");
			}
			System.out.println();
		}
		} // end class PriorityQ
		////////////////////////////////////////////////////////////////
// until one is smaller, { a[in] = a[in-1]; // shift item right, Insertion Sort 99 04 0672324539 CH03 10/10/02 9:12 AM Page 99 --in; // go left one position } a[in] = temp; // insert marked item } // end for }

public class PriorityQApp {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		PriorityQ thePQ = new PriorityQ(5);
		thePQ.insert(30);
		thePQ.insert(50);
		thePQ.insert(10);
		thePQ.insert(40);
		thePQ.insert(20);
		thePQ.display();
		while( !thePQ.isEmpty() )
		{
		long item = thePQ.remove();
		System.out.print("The item " +item + " is removed. ");// 10, 20, 30, 40, 50
		System.out.println(" ");
		thePQ.display();
		
		
		} // end while
		System.out.println(" ");
		} // end main()
		//-------------------------------------------------------------
		} // end class PriorityQApp




//HW#4



