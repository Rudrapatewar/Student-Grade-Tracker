package Task1;

import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.Iterator;
import java.util.Scanner;

public class Student {
	public static void main(String args[]) throws IOException
	{
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		System.out.println("How many Students");
		int n =Integer.parseInt(br.readLine());
		int a[]= new int [n];
		System.out.println("Enter those "+n+" Student grades");
		int i;
		for(i=0;i<a.length;i++) 
		{
			a[i]=Integer.parseInt(br.readLine());			
		}
		System.out.println("You entered  "+n+" Students grade");
		for(i=0;i<a.length;i++)
		{
			System.out.println(a[i]);
		}//for
		// for finding sum and average
		findall(a);				
	}//main
	static void findall(int a[])
	{
		int sum,i;
		float avg;
		int max =a[0];
		int min =a[0];
		for(i=0,sum=0;i<a.length;i++)
		{
			sum+=a[i];
			if (a[i]>max) {
				max =a[i];
			}
			if (a[i]<min) {
				min =a[i];
			}
		}//for
		avg=sum/(float)a.length;
		System.out.println("Sum of Student is = "+sum);
		System.out.println("Avgerage of students grade is ="+avg);
		System.out.println("Highest Marks are "+max);
		System.out.println("Lowest Marks are"+min);
	}//findall
 
}
