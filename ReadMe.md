# Java Note:

Run java in cmd, need to run cmd in adminstor, or it may not work
type cd c:\(need disk name) to locate the dirctory
first need to compile the JavaMain.java file,
second need to run java, java JavaMain (dont need to include .class)


# Java lab

# static to non-staic error

	class A{  
	 int a=40;//non static  

	 public static void main(String args[]){  
	  System.out.println(a);  // System.out.println is static method, so will have error, create an instance, then it will work
	 }  
	}     


# Java class structure:

	public class Car {

	//constructors
	  public Car (String pl) {
	  //initilization 
	  plate = pl;
	  }

	//methods always with prentsise

	//void means no need to return datatype
	public void displayCar() {
			System.out.print("Plate is " + plate + " with time of " + time + ", velocity is " + velocity);
		}
	// no void means need to return datatype
	public double calcAcceleration () {
			return accleration =  velocity /  time;
		}

	// main
	public static void main(String[] args) {

	  }
	}
	
# Scanner 
	Scanner is class.
	
# Constructor
	A constructor has the same name as the class name
	
# Java printf formatting
	https://www.geeksforgeeks.org/formatted-output-in-java/

# SQL different joins
	https://stackoverflow.com/questions/5706437/whats-the-difference-between-inner-join-left-join-right-join-and-full-join
	
# SQL entities and tables:
	https://www.quora.com/What-is-the-difference-between-entity-and-table-in-a-database
	
# Java static VS instance variable (give default value to variable).
	instance variable: String Name = '';

# Java file name and class name
	When changing the file name, should also change the class name, or file will not complile
	
# Java decimal formatting
	http://tutorials.jenkov.com/java-internationalization/decimalformat.html
	
# Java variables
	String str; this is the object, default value is null, so no memories.
	int a ; this is primitive, default value is 0. memory is allocated.
	int _test, $test are okay to compile but not recommended!
