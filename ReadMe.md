
# Java Note:

	Run java in cmd, need to run cmd in adminstor, or it may not work
	type cd c:\(need disk name) to locate the dirctory
	first need to compile the JavaMain.java file,
	second need to run java, java JavaMain (dont need to include .class)


# Java Ideas
	Use variables in the method, then in other class main method, instaniate other class object and use new object to call methods 		from other classes

	In Class One to call Class Two static method, can directly call Two.method(), no need to new object since it is static

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
	
# formating
	System.out.printf ("%10s|", "");
	//prinf
	%f for double/float => %10.2f
	%d for integer
	%s for String
	%n for newline
	
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

# Data type:
	primitive: 8
	reference: start with upper case like String
	void means not in two types


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
	
	Left Join and right join

	//use right table borrower_t to compare left table inventory_t
	select borrower_t.borrowername, inventory_t.bookid
	from borrower_t
	left join inventory_t
	on borrower_t.borrowerid = inventory_t.borrowerid

	//use right table inventory_t to compare left table borrower_t
	select borrower_t.borrowername, inventory_t.bookid
	from borrower_t
	right join inventory_t
	on borrower_t.borrowerid = inventory_t.borrowerid

# SQL differences between delete, trancate and drop
	delete                                            truncate                                          drop
	dml                                               ddl                                               ddl

	delete the data                                   delete the data                                   data gone
                                
	the table hhd space                               release the disk space                            disk sapce released
	and structure will remain                         structure remains                                 structure removed


# Java Array

	primitive array and reference type array
	Primitive:
	public int temperatureData [] = new int [TOTAL_NUMBERS];
	temperatureData[i] = randomNumber.nextInt(80+1)-40;
	non-primitive: 
	Client clients [] = new Client [numberOfClients];
	clients [i] = new Client();
	
# Scanner skipping nextLine() after use of other next functions
		//Code next()//
			System.out.print("Enter Employee FirstName LastName ");
			scanner.nextLine();
			String fullName = scanner.nextLine();
			System.out.print("Address ");
			String address = scanner.nextLine();
		//Output//
		Select type of employee: 1.Supervisor 2.Assistant 3.Driver
		1
		Enter Employee FirstName LastName
		
		//Code nextLine()//
			System.out.print("Enter Employee FirstName LastName ");
			String fullName = scanner.nextLine();
			System.out.print("Address ");
			String address = scanner.nextLine();

		//Output//
		Select type of employee: 1.Supervisor 2.Assistant 3.Driver
		1
		Enter Employee FirstName LastName Address
		
		see this: 
		https://stackoverflow.com/questions/13102045/scanner-is-skipping-nextline-after-using-next-or-nextfoo

# Java Unit Test
	String expectedName = "Ang";

	Person p = new Person ("Ang");

	assertEquals (expectedName, p.getName()); => return false;

	//good
	assertTrue(expectedName.equals(p.getName())); => best way to comapre objects
	//bad
	assertTrue(p.getNume().equals(expectedName));

	cannot import classes in the default
	
	
	If (object1.method() == object2.method()) { // use object1.method().equals(object2.method()), address of object is different

	} 
	
# Java Reference Type
	https://www.oreilly.com/library/view/java-8-pocket/9781491901083/ch04.html

	
# Java 2d array
	java


	2d array:
	int [][] 2dArray;
	2dArray = new int [rows][columns];

	2dArray is array of arrays
	2dArray = new [4][5];  4 rows 5 columns;
	2dArray = {{1,2,3},{4,5,6}};

	loop 2dArray;
	System.out.print("2dArray = {")
	for (int r = 0; r< 2dArray.length, r++) {
		System.out.print("{")
		for (int c = 0; c < 2dArray[r].length; c++) {
		2dArray [r][c] = r * (c+1);
		System.out.print(2dArray);
		if (c < (2dArray[r].length - 1)) {
		System.out.print(",")
		}
		}
		System.out.print("}")
		if (r < (2dArray[r].length - 1)) {
		System.out.print(", \n\t\t")
		}
	}
	System.out.print("};");

	int sum = 0;
	int prod =1;
	int countOfEven = 0;
	for (int[] r : 2dArray) {
		for (int c : r) {
		sum += c;
		prod *= c;
		if (c % 2 =0) {
		if (c % 2 = 0)
		++ countOfEven;
		countOfEven += 1;
	}
	}
	}


JAVA Sort OBJECTS BY PROPERTIES

# Override compareTo Method
	The compareTo method defines the natural order; the default way for ordering objects of a class.
	It should return a negative integer(usually -1), if the current triggering object is less than the passed one, and positive integer (usually +1) if greater than, and 0 if equal.
	public int compareTo(File b){ 
	    if(this.name > b.name) return 1; 
	    if(this.name < b.name) return -1;
	    else                   return 0;
	}

# Java compare string:
	.equals() compares value
	== comare reference
	https://www.javatpoint.com/string-comparison-in-java

# Java UML Sample
	http://pages.cs.wisc.edu/~hasti/cs302/examples/UMLdiagram.html
	
# JavaFX Notes
	http://tutorials.jenkov.com/javafx/index.html
	
# Commit first, then push
	
# Configure Oracle SQL Developer Connections
	0. cmd -> sqlplus sys/oracle as sysdba -> create user and previleges
	1.first location listener.ora file: C:\app\Wenbo\product\18.0.0\dbhomeXE\network\admin
	2.       (ADDRESS = (PROTOCOL = TCP)(HOST = DESKTOP-0OTGS6K)(PORT = 1522)) put HOST and PORT into
		 SQL Developer connection
	3. if Listener is not work, then go to task manager -> service -> start xe servic and stop ORCL

# web:

	xampp: root folder: htdocs
	index.php: first page loaded

	use url to access folders and files: localhost: 7331/folderName

	change xampp admin page: config -> server and port setting -> port to 7331 ssl to 4434

# Mobile Android Studio app cannot be installed
	https://www.youtube.com/watch?v=5gpjIKIbVWM
	
# Some small projects
	swing
	https://github.com/pythondever/swing-demo/blob/master/TankGame/Members.java
	
	swift
	https://github.com/nimomeng/30-swift-projects-in-30-days/tree/master/12.Emoji%20Slot%20Machine/Emoji%20Slot%20Machine

	angular
	https://blog.csdn.net/luodong1501/article/details/100106623
	
	deploy angular to aws
	https://medium.com/@sandeeptengale/deploy-angular-app-on-aws-ec2-instance-20749f17b33e
	

# User Debugger to check values and types

# Android Studio no such column Issue
	1.terminate app and delete database
	2. use this format 
	@Override
	    public void onCreate(SQLiteDatabase db)
	    {
		db.execSQL("CREATE TABLE " + TABLE_NAME + " (_id INTEGER PRIMARY KEY AUTOINCREMENT, MESSAGE text, SENT integer);");  // add or remove columns
	    }
	    
# Android sursorIndexOutOfBoundException Issue
	

	put *results.getColumnIndex(MyOpener.COL_MESSAGE) etc.* outside while loop
	Cursor results;
	int messageColumnIndex = results.getColumnIndex(MyOpener.COL_MESSAGE);
        int idColIndex = results.getColumnIndex(MyOpener.COL_ID);
        int sentColIndex = results.getColumnIndex(MyOpener.COL_SENT);
	
	put *results.getString(messageColumnIndex) etc.* within while loop
	
	while(results.moveToNext())
        {
            String message = results.getString(messageColumnIndex);
            long id = results.getLong(idColIndex);
            boolean sent = results.getInt(sentColIndex) == 1;

            //add the new Contact to the array list:
            elements.add(new Message(message, sent, id));
            printCursor(results,db.getVersion());

        }
	
# Android delete database
	1.put GoToADB.bat in the project folder
	2.run GoToADB.bat
	3.run sdb shell
	4.run-as projectname in mainfest
	5.cd to database
	

# JavaScript practice
	setInterval(function(){ document.getElementById('clickMe').click(); }, 240000);

# MySql Workbench add connection
	1. First connect to root user mysql workbench root password:0709
	2. Run sql script, new user with password and a new schema will be created
	3. Create a new connection with new password and user name, then only that schema will be kept

# oracle sqlplus login fails
	should check service to activate oracleservice
	
# timezone issue in java web application 
	https://stackoverflow.com/questions/37719818/the-server-time-zone-value-aest-is-unrecognized-or-represents-more-than-one-ti
	Second solution: n MySQL my.ini file set default-time-zone value bellow like

	Set default time zone
	default-time-zone = '+08:00'
	
