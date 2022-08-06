# Java-Basics
basics of java
package a;

public class Helloworld {
	public static void main(String[] args) {
		System.out.println("Hello World");
		
	//variable
		int a=5;
		a=10;
		System.out.println(a);
	/*Arithmetic + ,*, -,/,%
	 * Bitwise
	 * Relational
	 * Logical	
	 */
		int m=4 ,n=2;
		int	r=m+n;
		int	t=m*n;
		int	w=m%n;
		int	s=m/n;
				System.out.println(r);
				System.out.println(t);
				System.out.println(w);
				System.out.println(s);
				

				//ifElse
				int q=7;
				if(false)
					System.out.println("hello");
				if(true)
					System.out.println("bye");
				
				
			int v=7;	
			if(v%2==0)
			{
				System.out.println("even");
			}
			else if(v%2!=0)
			{
				System.out.println("odd");
			}
			else
			{
				System.out.println("nothing");
			}
			//ternaryOperator
			//? exp1:exp2
			int x=5;
			int y=3;
			y=x>6?1:2;
			System.out.println(y);
			
			//Switch
			int d=3;
			switch(d)
			{
			case 1:
				System.out.println("one");
			break;
			case 2:
				System.out.println("two");
			break;
			case 3:
				System.out.println("three");
				break;
				default:
					System.out.println("no match");
					 
					//While & For Iteration Statement
				//while , do while,for
					int i=1;
					while(i<=5)
					{System.out.println("hellow");
					i++;
					}
			int p=9;
			do
			{System.out.println("hello");
			i++;
			}while(p<=5);
			}
			for(int u=1;u<=5;u++)
				{System.out.println("hello");
				}
	
	
	//nested Loops
/*
 * * * * 
 * * * *
 * * * *
 * * * *
 */
	for (int g=1;g<=4;g++)		
	{for(int f=1;f<=4;f++)
	{
		System.out.println("*");
	System.out.println("*");
	}}
	//break, continue
	for (int o=1;o<=10;o++)
	{if (o==7)
	{continue;}
	System.out.println("value is" +o);
	}
	for (int e=1;e<=10;e++)
	{if (e==7)
	{break;}
	System.out.println("value is" +e);
	}
	
	}}
	


package encapsulation;
class Student{
	int rollno;
	String name;
	//getters and setters
	public int getRollno() {
		return rollno;
	}

	public void setRollno(int rollno) {
		this.rollno = rollno;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}}
	
public class Encapsulation {
public static void main(String[] args) {
	Student s1=new Student();
	s1.setRollno(2);
	s1.name="sawera";
System.out.println(s1.getName());
}}



package varargs;
class Calc
{public int add(int ... n) //as an array we can add many variables by int and 3 dots
	{
	int sum=0;
	for (int i : n)
	{
		sum=sum+i;
	}
		return sum;
	}
	}
public class Varargs {
	public static void main(String[] args)
	{
		Calc obj = new Calc();
		System.out.println(obj.add(4,5,6,7,8,9,1,2));
		
	}

}

class A{
	public void show() {
		System.out.println("in A");
	}
}
class B extends A //inheritance
{
	@Override
public void show() {
	System.out.println("in B"); //method overriding of A
}	
}
package obj;
class Calc
{
int num1;
int num2;
int result;
 public Calc()
 {
	num1=5;
	num2=5; 	
	System.out.println("in constructor");
 }
	public Calc(int n) //multiple constuctor can be make with different signatures
	{
		this.num1=n; //num1 is not local variable if we add this.
		this.num2=n;
	}
 }
public class ObjectDemo {
public static void main(String[] args) {
Calc obj=new Calc(); //constuctor
System.out.println(obj.num1);
}
}

package staticDemo;
class emp{
	int id;
	int salary;
	static String ceo; //static=same for all objects
	public void show()
	{
		System.out.println(id + " : " + salary + " : " + ceo);
	}
}
public class StaticDemo {
	public static void main(String[] args) {
		emp sawera=new emp();
		sawera.id=26;
		sawera.salary=600000;
		sawera.ceo="Fazal";
		emp ayesha= new emp();
		ayesha.id=15;
		ayesha.salary=500000;
		ayesha.ceo="Fazal";
		ayesha.ceo="rubina"; // also we can write emp.ceo as it is same for all objects
		sawera.show();
		ayesha.show();
	}

}
package operators;

public class ArithmeticDemo {
	public static void main(String[ ] args) {
		int result=1+2;
		System.out.println("1 + 2 = "+ result);
		int original_result=result;
		
		result=result-1;
		System.out.println(original_result + "-1 " + result);
		 original_result=result;
		
		result=result*2;
		System.out.println(original_result +"*2 "+result);
		original_result=result;
		System.out.println(original_result);
				
	}

package nestedforloops;

public class NestedForLoops {
public static void main(String[] args ) {
	int arr[][]= {{2,7,9},{3,6,1},{7,4,2}};
	for(int i=0; i<3; i++) {
		for(int j=0; j<3; j++) {
			System.out.println(arr[i][j]+" ");
		}
		System.out.println();
	}
}
}

package arraylist;

import java.util.ArrayList;

public class Arraylist {
	public static void main(String[] args) {
	List<Integer>arrayList=new ArrayList<Integer>(5);
	for (int i=1; i<=5; i++) {
		arrayList.add(i);
	}
	System.out.println(arrayList);
	arrayList.remove(3);
	System.out.println(arrayList);
	for (int i=0; i< arrayList.size; i++)
		System.out.println(arrayList.get(i)+" ");
	}
	}


package linkedlistdemo;

import java.util.LinkedList;

public class LinkedListDemo {
	public static void main(String args[]) {
	LinkedList<String>list=new LinkedList<String>();
	list.add("A");
	list.add("B");
	list.addLast("C");
	list.addFirst("D");
	System.out.println(list);
	
	list.add(2,"E");
	System.out.println(list);

	list.remove("B");
	System.out.println(list);
	}
	}


package hashsetdemo;
import java.util.*;
public class HashsetDemo {
public static void main(String[] args) {
Set<String>hashSet=new HashSet <>();
hashSet.add("A");
hashSet.add("B");
boolean r1=hashSet.add("C");
System.out.println(r1);
boolean r2=hashSet.add("C");
System.out.println(r2);
System.out.println(hashSet);
System.out.println("list contains c or not?"+hashSet.contains("c"));

}}

public class Object {
	public static void main(Object[] args ) {
	Object[] anArray;
	anArray= Object[2];
	anArray[0]=100;
	anArray[1]=200;
	anArray[2]="sawera";
	System.out.println("element at index 0: "+ anArray[0]);
	}
}



package whileDemo;

public class WhileDemo {
	public static void main(String[] args) {
		int count=1;
		while (count<10) {
			System.out.println("Count is:" + count);
			count++;
			
		}
	}
	

}
public class Unary_Demo {
public static void main(String[] args) {
	int result=+1;
	System.out.println(result);
	result--;
	System.out.println(result);
	result++;
	System.out.println(result);
	result=-result;
	System.out.println(result);
	boolean success = false;
	System.out.println(success);
	System.out.println(!success);
	
	
	int i=3;
	System.out.println(i);
	i--;
	System.out.println(i);
	i++;
	System.out.println(i);
	i=-i;
	System.out.println(i);
	boolean s = false;
	System.out.println(s);
	System.out.println(!s);
	
}

}
public class Twodarray {
	public static void main(String args[]) {
	int arr[][]= {{2,7,9},{3,6,1},{7,2,4}};
	for (int i=0; i<3; i++) {
		for(int j=0;j<3;j++) {
			System.out.println(arr[i][j]+" ");
		}
		System.out.println();
	}
	}

}
package ternaryoperator;

public class Ternaryoperator {
public static void main(String[] args) {
	int a=5;
	int b=3;
	int result;
	result=a>b? a:b;
	System.out.println(result);
}
}

package bitWiseOperator;

public class bitWiseOperator {
	public static void main(String[] args){
		int a= 5;
		int b=7;
		System.out.println("a&b= "+(a & b));
		System.out.println("a|b=  " + (a|b));
		
			
		
	}

}
public class ComparisionOperator {
	public static void main(String[] args) {
		int value1=1;
		int value2=2;
		if (value1 == value2) {
		        System.out.println("value1 == value2");}
		if (value1 != value2) {
				System.out.println("value1 != value2");}
		if (value1 > value2) {
			System.out.println("value1 > value2");}
		if (value1 < value2) {
			System.out.println("value1 < value2");}
				
			
	}

}
package enhancedforloop;

public class EnhancedForLoop {
	public static void main(String[] args) {
		int[] numbers= {1,2,3,4,5,6,7,8,9,10};
		for (int i: numbers) {
			System.out.println("ccount is: " +i);
			
		}
	}

}
package oneDArray;

public class OneDArray {
	public static void main(String[] args) {
	int[] arr=new int[4];
	arr[0]=10;
	arr[1]=20;
	arr[2]=30;
	System.out.println(arr[0]);
}
		

}
package ifElseDemo;

public class ifElseDemo {
public static void main(String[] args) {
	int score=76;
	char grade;
	if (score>=90) {
		grade='A';

}else if(score>=80) {
		grade='B';
}else if(score>=70) {
	grade='c';
}else if(score>=60) {
	grade='D';
}else {grade='F';
} System.out.println("grade= "+ grade);}}



package multidimentional;

public class MultidimentionalArray {
	public static void main(String[] args) {
		int[][][] arr= {{{1,2,10},{3,4,11}},{{5,6,12},{7,8,13}}};
		System.out.println(arr[1][1][2]);	}

}
package nestedIf;

public class nestedIf {
	public static void main(String[] arg) {
		int num=50;
		if (num==50) {
		System.out.println("num= "+num);
		if(num<70) {
			System.out.println("num is less than the 70");
			if (num<55) {
				System.out.println("num is less than 55");
			}
		}
		
	}

}
}




