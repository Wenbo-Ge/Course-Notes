# Java Note:

Run java in cmd, need to run cmd in adminstor, or it may not work
type cd c:\(need disk name) to locate the dirctory
first need to compile the JavaMain.java file,
second need to run java, java JavaMain (dont need to include .class)


# Java lab

# static to non-staic error

	when declare the variable with public outside of a method ():
		public int time = 10;
	then for the method function should start with public (start with public static will have conflicts):
		public void displayCar() {
		System.out.print("Plate is " + plate + " with time of " + time + ", velocity is " + velocity);
		}

	or just declera varible in the method.


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
	
# Java static VS instance variable (give default value to variable).
	instance variable: String Name = '';
	
	
