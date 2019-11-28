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
	
# Java private variable vs pulic variable
	class One {
		private String content; // private variable cannot be directly used in other class, but can put variable into public 			method then called by other classes
		public void display () {
			content = "aa"
		} // private can be used in pulic method then method can be called in other classes
	}
	class Two {
		One call = new One();
		sysout.print(call.content) // this won't work because of private variable
		call.display() //will work becasue of pulic method
	}
	
# SQL deleting and dropping order:
	child is frist then parent (in terms of foreign key)

# java else if:
	Use the else if statement to specify a new condition if the first condition is false.

	if (condition1) {
	  // block of code to be executed if condition1 is true
	} else if (condition2) {
	  // block of code to be executed if the condition1 is false and condition2 is true
	} else {
	  // block of code to be executed if the condition1 is false and condition2 is false
	}

# java casting:
	small to large will be automated converted: 5 to "5" 
	large to small must use conversion Double.parse("")

# java field vs variable:
	Field is a data member of a class. A field is non static, non-transient instance variable. Field is generally a private variable 	on an instance class. Variables are comprised of fields and non-fields

	
# Sql
	--Test
	select * from part_ext_t
	INSERT INTO Part_EXT_T( Part, Material, Size, Cost ) VALUES( 'BOLT', 'BRASS', 'SMALL', null );
	INSERT INTO Part_EXT_T( Part, Material, Size, Cost ) VALUES( 'WASHER', 'BRASS', 'SMALL', null );
	INSERT INTO Part_EXT_T( Part, Material, Size, Cost ) VALUES( 'NUT', 'BRASS', 'SMALL', null );

	select count(*), count(cost), avg(cost)
	from part_ext_t 

	//group functions like count will ignore the null value;

	select coalesce (cost, 0) from part_ext_t // replace null with 0;
	

