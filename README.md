import java.io.*;
import java.util.Scanner;

public class ControlStructures {
	public static void main(String[] args) {
		Scanner input = new Scanner(new InputStreamReader(System.in));
		int choice;
		System.out.println("\t\t\tControlStructures\n\t\t\t*****");
		System.out.println("1.Selection\n2.Iteration\n3.Jump\n4.Exit");
		System.out.println("Input your choice:");
		choice = input.nextInt();
		switch(choice) {
		case 1: System.out.println("Entered:"+choice);
		  		System.out.println("Selection statememnts\n*****");
		  		System.out.println("1.If Else\n2.Switch\nMake u r Selection:");
		  		choice = input.nextInt();
		  		if(choice == 1)
		  		{
		  			System.out.println("Example program on if else that determine whether a number is positive or nagative");
		  			System.out.println("Input a number");
		  			int number = input.nextInt();
		  			if(number<0)
		  				System.out.println(number+"is negative");
		  			else
		  				System.out.println(number+"is positive");
		  		}
		  		else
		  		{
		  			System.out.println("Example program on switch that determine whether a number is male or female");
		  			System.out.println("Input a number(MALE-1 FEMALE-0:)");
		  		int number = input.nextInt();
		  		switch(number)
		  		{
		  		case 0: System.out.println("Person is FeMale");
		  		   		break;
		  		case 1: System.out.println("Person is Male");
		  		 	 	break;
		  		default:System.out.println("Invalid Choice");
		  		 		break;
		  		
		  		}
		}
		break;
		case 2: System.out.println("U Entered:"+choice);                       
		        System.out.println("\nIteration statements\n******");
		        System.out.println("1.while\n2.for\n3.do..while\nMake Ur selection:");
		       choice = input.nextInt();
		       if(choice == 1)
		       {
		    	   System.out.println("Example program on While\n Displays only Even Numbers up to range");
		    	   int n = input.nextInt();
		    	   int i=1;
		    	   System.out.println("Even numbers in the range 2 and "+n+"are");
		    	    				while(i<=n)
		    	    				{
		    	    					if(i%2==0)
		    	    						System.out.println(i+"\t");
		    	    					i++;
		    	    				}
		       }
		       else if(choice == 2)
		       {
		    	   System.out.println("Example program on for\n Displays only Even Numbers up to range");
		    	   int n = input.nextInt();
		    	   System.out.println("Even numbers in the range 2 and "+n+"are");
		    	    		for(int i=1;i<=n;i++)
		    	    		{
		    	    			if(i%2==0)
		    	    				System.out.println(i+"\t");
		    	    		}
		       }
		       else
		       {
		    	   System.out.println("Example program on Do..While\n Displays only Even Numbers up to range");
		    	   int n = input.nextInt();
		    	   int i=1;
		    	   System.out.println("Even numbers in the range 2 and "+n+"are");
		    	    				do
		    	    				{
		    	    					if(i%2==0)
		    	    						System.out.println(i+"\t");
		    	    					i++;
		    	    				}while(i<=n);
		       }
		       break;
		       case 3: System.out.println("Entered:"+choice);
				System.out.println("\njump statements\n*****");
				System.out.println("1.break\n2.continue\nMakeU r selection:");
				choice = input.nextInt();
				if(choice ==1)
				{
					System.out.println("Example program on break statement.\nThough the loop is written to display numbers from 1 to 10,but is exited when i becomes 4.");					for(int i=1;i<=10;i++)
					{
						if(i==4)
							break;
						System.out.println(i+"\t");
					}
		       }
			   else
			   {
				   System.out.println("Example program on continue statement.\nExcept 4 this code snippet output 1 to n 10");
				   for(int i=1;i<=10;i++)
				   {
					   if(i==4)
						   continue;
					   System.out.println(i+"\t");
				   }
			   }
				break;
		case 4: System.exit(0);
	   }
	   input.close();
     }
}
