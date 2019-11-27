## Crafting Quality Code 
Trainer:  Naveen Kumar 
Company: Philips 
Nov2019 


Day 1 
	clean code practices 
		understandable
		maintanable 
		readable 
		less complex 
		easy to extend 
		reusable 
		enough comments 
		meaning full namings 
		testable code 
		avoid duplications 
		avoid memory leaks 
		
		class Math{
		// this method returns factorial of a number 
		// given an int 
			public int factorial( int n ){
			
			}
			
		}
		
		IST 
		
		we work with 
		1. Who has domin knowledge 
		2. who has technology knowlege 
		3. who knows technology and domain 
		
		
		
		Convenstion 
		
		methods  - camel case (setName, paySalary)
		variables - camel case(employeeNumber, employeeId,  employeeName, __)
		constants - UPPERCASE, _ 
		class - PascalCasing (Employee)
		enums - UPPERCASE 
		interface - IEmployee
		
		
		
		com
			onsite
				ny
				class Salary{
				}
				
				ca
				class Salary{
				}
				
				va
				class Salary{
				}
				
				or
				class Salary{
				}
				
				
				
		import com.onsite.ny.Salary; 
		Salary s = new Salary(); 		
				
			
		sellmystuffs.com 
		hidesign 
				
				
				
				
			offshore
		class Salary{
		}
		
		class SalaryOffshore{
			
		}
		
		class SalaryOnsiteEngland{
			
		}
		
		class SalaryOnsiteIndiaKarnataka{
			
		}
		
		
		// for US 
		class Employee{
			private int employeeId; 
			private Name name; 
			private String salaray; 
		}
		
		class Customer{
			private int customerId; 
			private Name name;
			private double income; 
		
		}
		
		
		class Name{
		private String firstName; 
		private String lastName;
		}
		
		
		
		void main(){}
		
		
		
		
		
		
		
		// for India 
		class Employee{
			private int employeeId; 
			
			private String salaray; 
		}
		
	
// 300 	


enum CARNAME{
	MARUTI, AUDI, BMW
}

// all your generic properties will go here 
class Car{

	public Car(){}
	
	
	public static Car createCar(CARNAME carName){
		switch(carName){
			case MARUTI: 
				return new Maruti(); 
			case AUDI:
				return new Audi(); 
			case BMW: 
				return new BMW(); 
		}
	}
}
class BMW extends Car{
	public BMW(){
		super();
	}
}

class Maruti extends Car{
}

class Audi extends Car{
}

class Hyundai extends Car{
}	
		
		
class Player{
	public void playMusic(Car c ){
		c.play(); 
		c.stop();
		c.paus();
	}
			
}
		
			
		
		
version 1. -> sony 	
		
BMW b1 = new BMW(); 
Maruti m1 = new Maruti(); 
Audi a1 = new Audi(); 
		
version 2. -> Sony 

Car c1 = new BMW(); 
c1 = new Maruti(); 
c1 = new Audi(); 	
		
		
		
version 3. -> Sony 
Car car = Car.createCar(CARNAMES.AUDI); 
car = Car.createCar(CARNAMES.MARUTI); 
car = Car.createCar(CARNAMES.BMW); 

		
	
-- return or not return 

// version 1 

class EmployeeDAO{
	public boolean insertEmployee(Employee employee){
		// open connection 
		
		// process 
		// return  exeucteUpdate > 0 
		
		// clse connection 
	}
}	
		
		
	
class EmployeeDAOTest{
	
	@Test
	public void insertEmployeeTest(){
		boolean expected = true; 
		EmployeeDAO employeeDAO = new EmployeeDAO(); 
		boolean actual = employeeDAO.insertEmployee(new Employee(...));
		assertEquals(expected, actual);  
	}
}


version 2 

class EmployeeDAO{
	public void insertEmployee(Employee employee){
		// open connection 
		
		// process 
		//   exeucteUpdate > 0 
		
		// clse connection 
	}
	
	// null 
	public Employee getEmployee(int employeeId){
		// open connection 
		use result set 
		// return new Employee(); 
		// close connection 
	}
	
	
}	
		


	
class EmployeeDAOTest{
	
	@Test
	public void insertEmployeeTest(){
		int id = 101; 
		String name = "Harry"; 
		
		Employee emp = new Employee(id, name);
		EmployeeDAO employeeDAO = new EmployeeDAO(); 
		employeeDAO.insertEmployee(emp); 
		
		
		Employee employee = employeeDAO.getEmployee(id); 
		assertEquals(emp, employee); 
	}
}



class A{
	public A(){}
}


class B extends A{

	public B(){
		super(); 
	}
}



class B {
	A a; 
	public B(boolean flag){
		a = new A(); 
	}
	
	
}

B b = new B(); 


		
		
Patient Mangement 
1. persisting data - file 
	a. patient name, age, height, weight, dob, gender, implants, contact, 
	   emergency contact, blood group, 
2. persisting data (doctor) - file 
	// doctors data 
3. prescription 
	doctor - patient 

4. test cases (TDD) 
5. structure
6. documentation (dev / user)
7. contracts 
8. security 


entity / beans / bean 
interfaces / contract 
dao 
util 
impl / app / main 
TDD 
test 

		
		
		
		
		
if(a> b && a > c){
	a is large 
}else if(b > c ){
	b is large 
}else {
	c is large 
}
		
		
		
		
Reader / Writer  - char 
	Patient - p.getpId(); p.getName().getFirstName(); p.getName().getLastName(); 
	
InputStream / OutputStream - byte 
	Patient - p 

		
OOS  - p1 (ser)
OOS - p2 (ser)
oos - p3 (ser)



https://github.com/adithnaveen
https://github.com/adithnaveen/philips-clean-code-practice-nov-2019
		
		
		
		
		
		
		
		
		
Day 2 



	if(name == ShapeNames.CIRCLE) {
			return new Circle(); 
		}
		
		if(name == ShapeNames.RECTANGLE) {
			return new Rectangle(); 
		}
		
		if(name == ShapeNames.TRIANGLE) {
			return new Triangle(); 
		}
		
		return null;
		

public class Student {
	private int studentId; 
	private String studentName; 
	private double percentage; 
	
	public Student(int studentId, String studentName, double percentage){
		// assign 
	}

		// getters
}
		
		
Student student = new Student(101, "Harry", 3434); 


sop(student) -> 123 

student.setStudentName("Peter"); 
sop(student) -> 123 








	year = car.year;

//		if(car.enginee instanceof TurboEngiee) {
//			enginee = new TurboEngiee( (TurboEngiee) (car.enginee)); 
//		}else {
//			enginee =  new Enginee(car.enginee);
//		}

		// we are not copy of clone, as that has the problem.
		enginee = car.enginee.copy();





		// this will not work since java does not give copy constructor
		Car car2 = new Car(car1);
		System.out.println(car2);






Enginee Created... 
Turbo Enginee created... 
	Car [year=2019, enginee=com.philips.abstractfactory1.TurboEngiee  : 2018699554]
	Car [year=2019, enginee=com.philips.abstractfactory1.Enginee  : 1311053135]


Enginee Created... 
Turbo Enginee created... 
	Car [year=2019, enginee=com.philips.abstractfactory1.TurboEngiee  : 2018699554]
	Car [year=2019, enginee=com.philips.abstractfactory1.TurboEngiee  : 1311053135]



Enginee Created... 
Piston Enginee created... 
Car [year=2019, enginee=com.philips.abstractfactory1.PistonEnginee  : 2018699554]
Car [year=2019, enginee=com.philips.abstractfactory1.Enginee  : 1311053135]

Enginee Created... 
Piston Enginee created... 
Car [year=2019, enginee=com.philips.abstractfactory1.PistonEnginee  : 2018699554]
Car [year=2019, enginee=com.philips.abstractfactory1.PistonEnginee  : 1311053135]


		
		
Day 3 

documentation rules 
https://www.tiobe.com/documentation/

TICS Supported tools 
https://www.tiobe.com/tics/fact-sheet/

// provided if you have the valid login (paid) 
https://portal.tiobe.com/2019.3/docs/user/eclipse.html




To know cyclomatic complexity of C++ Code 
https://marketplace.eclipse.org/content/metriculator#group-external-install-button



https://docs.sonarqube.org/7.8/analysis/scan/sonarscanner-for-maven/
https://bit.ly/2KPUIWf


Sample projects of sonar 
https://github.com/SonarSource/sonar-scanning-examples.git

simple maven project
https://github.com/SonarSource/sonar-scanning-examples/tree/master/sonarqube-scanner-maven/maven-basic





Day 3 Notes 
---------------------

chetan.dayapule@philips.com
chetan.dayapule@gmail.com
nagendra.varikuti@philips.com
nagendra.varikuti@gmail.com


it is a structural metrics which mesure inter-module complexitites. 

fan-in : is the number of modules that call a given module
fan-out : is the number of modules that called by a given module 

ashish.gupta@manipalglobal.com


for c++ its pure virtual function 
others interface 

interface Observer 
	public void update(); 


for c++ its pure virtual function 
others interface 

interface Observable 
		public void addUser(Observer o); 
		public void removeUser(Observer o); 
		public void notifyAllObservers(); 
		
		

class IPhone implements Observable 
	// the value will be null 
	List<Observers> users; 
	boolean arrived = true; 
	
	IPhone(){
		users = new ArrayList<>; 
	}
	
	
	public void addUser(Observer o){
		users.add(o); 
	}
	public void removeUser(Observer o){
		users.remove(o); 
	}
	public void notifyAllObservers(){
		// we will notify all the users who has registered with us 
		for(Observer user: users){
			user.update(); 
		}
	}
	
	// we have to implement the logic to check the arrival 
	public boolean isArrived(){
		return arrived; 
	}
	
	public void setArrived(boolean arrived){
		this.arrived = arrived; 
		notifyAllObservers(); 
	}
	
	
	
}


class IPadPro implements Observable 
	// the value will be null 
	List<Observers> users; 
	boolean arrived = true; 
	
	IPadPro(){
		users = new ArrayList<>; 
	}
	
	
	public void addUser(Observer o){
		users.add(o); 
	}
	public void removeUser(Observer o){
		users.remove(o); 
	}
	public void notifyAllObservers(){
		// we will notify all the users who has registered with us 
		for(Observer user: users){
			user.update(); 
		}
	}
	
	// we have to implement the logic to check the arrival 
	public boolean isArrived(){
		return arrived; 
	}
	
	public void setArrived(boolean arrived){
		this.arrived = arrived; 
		notifyAllObservers(); 
	}
	
	
	
}



class System implements Observer{
	
}



class User implements Observer{
	private Observable observable; 
	private String name; 
	
	public User(Observable observable, String name){
		this.observable = observable; 
		this.name =name; 
	}
	
	 
	
	public void buyIPhone(){
		print "Hurray i bought iphone - " + name
	}
	
	public void unsubscribe(){
		observable.remove(this);
	}
}


class App/Client{
	main(){
		// we can have multiple observable 
		Observable iphoneObs = new IPhone(); 
		Observable iPadPro = new IPadPro(); 
		
		Observer pragathi = new User(iphoneObs, "Pragathi"); 
		Observer naveen = new User(iphoneObs, "Naveen"); 
		Observer prathima = new User(iphoneObs, "Prathima"); 
		Observer midhun = new User(iphoneObs, "Midhun"); 
		
		iphoneObs.addUser(pragathi); 
		iphoneObs.addUser(naveen); 		
		iphoneObs.addUser(prathima); 		
		iphoneObs.addUser(midhun); 		
		
		((IPhone)iphoneObs).setArrived(true); 
		
		
	}
}




S - Single Reponsibility Principle 
	A class should have one, and only one, reason to change 

O - Open Close Principle 
	You should be able to extend the class behaviour, without modifying it 

L - Liskov Substitution Principle 
	Derived classes must be sustituted for their base classes 

	class A {
		hi(){}
	}
	
	class B {
		hi(){}
	}



I - Interface Segregation Principle 
	Make fine gride interface/s that are client specific 
	Your interfaces shall not be  thick / fat 

D - Dependency Inversion Principle 
	Depends on abstraction, not on concretion 
	
interface Animal {}

class Human implements Animal {}
class Tiger implements Animal {}
class Cheetah implements Animal {}

class Behave{
	walk(Animal animal){
	}
}




--------- Visitor Pattern------------ 
This is one the behavioural design patterns, when we have to perform an operation on a group
of similar kind of objects. 


// visitable 

interface Buyable {
	public double buy(Products product); 
}


class Fuel implements Buyable{
	private int price; 
	
	public Fuel(int price){
		this.price = price; 
	}
	
	public int getPrice(){
		return price; 
	}
	

	public double buy(Products product){
		return product.buyProduct(this);
	}
}


class Luxury implements Buyable{
	private int price; 
	
	public Luxury(int price){
		this.price = price; 
	}
	
	public int getPrice(){
		return price; 
	}
	

	public double buy(Products product){
		return product.buyProduct(this);
	}
}


class Needs implements Buyable{
	private int price; 
	
	public Needs(int price){
		this.price = price; 
	}
	
	public int getPrice(){
		return price; 
	}
	

	public double buy(Products product){
		return product.buyProduct(this);
	}
}


interface Products {
	double buyProduct(Luxury luxury);
	double buyProduct(Fuel fuel);
	double buyProduct(Needs needs);		
}


class RuralPlaces implements Products{
	
	// to be initialized 
	
	public RuralPlaces(){
	}
	
	public double buyProduct(Luxury luxury){
			print("Luxury Comes with Tax ")
			return luxuxy.getPrice()*0.20; 
	}
	public double buyProduct(Fuel fuel){
		print("Fuel Comes with Tax ")
		return luxuxy.getPrice()*0.12;
	}
	public double buyProduct(Needs needs){
		print("Basic Neds Comes with Tax ")
		return luxuxy.getPrice()*0.0;
	}
}



class UrbanPlaces implements Products{
	
	// to be initialized 
	
	public UrbanPlaces(){
	}
	
	public double buyProduct(Luxury luxury){
			print("Luxury Comes with Tax ")
			return luxuxy.getPrice()*0.30; 
	}
	public double buyProduct(Fuel fuel){
		print("Fuel Comes with Tax ")
		return luxuxy.getPrice()*0.18;
	}
	public double buyProduct(Needs needs){
		print("Basic Neds Comes with Tax ")
		return luxuxy.getPrice()*0.07;
	}
}



class App{
	main{
		RuralPlaces ruralPlaces = new RuralPlaces(); 
		UrbanPlaces urbanPlaces = new UrbanPlaces(); 
		
		Fuel petrol = new Fuel(77); 
		Luxury stay = new Luxury(3500); 
		Needs water = new Needs(10); 
		
		
		print ruralPlaces.buyProduct(petrol); 
		print ruralPlaces.buyProduct(stay); 
		print ruralPlaces.buyProduct(water); 				
		
		
		print "-----------------------------------------------------"
		
		print urbanPlaces.buyProduct(petrol); 
		print urbanPlaces.buyProduct(stay); 
		print urbanPlaces.buyProduct(water); 				
		
		
	}
}





Proxy Pattern 
--------------------


// any business logic ideally it will be for logger / security or utilities 
class Aspect{
	public void loggingAspect(){
		
		print "Hey i'm from loggin aspect";
	}
}


class Rectangle {
	private int len; 
	private int bre; 
	
	// getters and setter 
	// accessors and mutators 
}


class Triangle{
	private int len; 
	private int bre; 
	
	// getters and setter 
	// accessors and mutators
}


class ShapeService{
	private Rectangle rectangle; 
	private Triangle triangle; 
	
	public void setRectangle(Rectangle rectangle){
		this.rectangle = rectangle; 
	}
	
	public void setTriangle(Triangle triangle){
		this.triangle = triangle; 
	}
	
	// getters 
	public Triangle getTriangle(){
		return triangle; 
	}
	
	public Rectangle getRectangle(){
		return rectangle;
	}
	
	
}


class ShapeServiceProxy extends ShapeService{
	
	// getters 
	public Triangle getTriangle(){
		new Aspect().loggingAspect();
		return new Triangle(); 
	}
	
	public Rectangle getRectangle(){
		new Aspect().loggingAspect();
		return new Rectangle();
	}
	
}



class FactoryService{
	public Object getObject(String objectType){
		if(objectType == "triangle"){
			return new ShapeServiceProxy().getTriangle();
		}else if(objectType == "rectangle"){
			return new ShapeServiceProxy().getRectangle();
		}else 
		
		if(objectType == "shapeservice"){
			return new ShapeService(); 
		}else if(objecType =="shapeserviceproxy"){
			return new ShapeServiceProxy(); 			
		}
		
		
		return null; 
	}
}

class App {
	main(){
		//good idea would be to make it static 
			FactoryService factory = new FactoryService(); 
		
			ShapeService service = (ShapeService) factory.getObject("shapeservice"); 
			
			Triangle t1 = service.getTriangle(); 
			
			// if you want proxy triangle or rectangle 
			ShapeServiceProxy serviceproxy = (ShapeServiceProxy) 						factory.getObject("shapeserviceproxy"); 
			
			Triangle t2 = serviceproxy.getTriangle(); 
			
		}
}







https://bit.ly/37wpsFf



sonar-project.properties

sonar.projectKey=clean-code
sonar.projectName=Philips Clean Code 
sonar.projectVersion=1.0 
sonar.sources=src
sonar.sourceEncoding=UTF-8



Day 4 
---------------------



codescene.io 

Tutorials
guides -> https://codescene.io/docs/guides/index.html
hotspots -> https://codescene.io/docs/guides/technical/hotspots.html
getting started -> https://codescene.io/docs/getting-started/index.html
















