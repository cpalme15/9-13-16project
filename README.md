import java.util.*;

/*Programmers:Collin Palmer, Zachariach Pelletier
 * Date:9/13/16
 * COSC 111
 * Purpose: To calculate the Weight, length, and engines required for any 
 * train of any given amount of the separate cars
 */
public class Rail2 {
	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Scanner keyboard = new Scanner(System.in);
	     System.out.println("This program is written by Collin Palmer and Zane Pelletier");
		
		System.out.println("The number of Box car is:");
		      int boxcars= keyboard.nextInt();
		
		System.out.println("The number of Gondolas is:");
		      int gondola= keyboard.nextInt();
		
		System.out.println("The number of Passenger cars is:");
		      int passenger= keyboard.nextInt();
		      int totalofcars=(boxcars+gondola+passenger);
		 
		System.out.println("The train is "+totalofcars+" cars long and consists of:");
		System.out.println(boxcars+" box cars");
		System.out.println(gondola+" gondola cars");
	    System.out.println(passenger+" passenger cars");
		      int totalweightofcars=(boxcars*53+gondola*65+passenger*70);
		      float totalweightoftrain=(totalweightofcars+52);
		      int totallengthoftrain=(int) (boxcars*45.0+gondola*70.0+passenger*80.5+55.0);
		      double exacteng=Math.ceil(totalweightoftrain/1000.0);
		     
		      
		      
        System.out.println("The total weight of the of the cars is "+ totalweightofcars +" tons.");
        System.out.println("The number of engines required is "+exacteng+".");
        System.out.println("The total weight of the entire train is "+totalweightoftrain+" tons.");
        System.out.println("The total train is "+totallengthoftrain+" feet long.");
        keyboard.close();
	}   

}
