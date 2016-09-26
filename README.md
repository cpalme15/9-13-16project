	import java.util.*;

/*Programmers:Collin Palmer, Zachariach Pelletier

Date:9/13/16
COSC 111
Purpose: To calculate the Weight, length,
and engines required for any
train of any given amount of the separate cars */ 
public class Rail2 
    {

    public static void main(String[] args) { // TODO Auto-generated method stub

    Scanner keyboard = new Scanner(System.in);
    int boxcars=0;
    int gondola=0;
    int passenger=0;
 	int totalofcars=(boxcars+gondola+passenger);
 	final int boxweight=53;
 	final int gonweight=65;
 	final int passweight=70;
 	final double boxlen=45.0;
 	final double gonlen= 70.0;
 	final double passlen=80.5;
 	final double englimit=1000.0;
 	final double something=55.0;
 	int totalweightofcars=(0);
 	final int engweight=52;
 	float totalweightoftrain=0;
 	double totallengthoftrain=0;
 	double exacteng=0;
 	float trainweightwoeng=0;
 	
 	System.out.println("Enter how many boxcars.");
	 boxcars= keyboard.nextInt();
	 System.out.println("Enter how many gondola.");
 	 gondola= keyboard.nextInt();
 	 System.out.println("Enter how many passenger.");
 	 passenger= keyboard.nextInt();
 	totalweightofcars=(boxcars*boxweight+gondola*gonweight+passenger*passweight);
    totalweightoftrain=(totalweightofcars+engweight);
    trainweightwoeng=(totalweightoftrain-engweight);
    totallengthoftrain=(boxcars*boxlen+gondola*gonlen+passenger*passlen+something);
    exacteng=Math.ceil(trainweightwoeng/englimit);
 	
    
    System.out.println("This program is written by Collin Palmer and Zane Pelletier");
 	System.out.println("The number of Box car is:");
 	System.out.println("The number of Gondolas is:");
 	System.out.println("The number of Passenger cars is:");
 	System.out.println("The train is "+totalofcars+" cars long and consists of:");
 	System.out.println(boxcars+" box cars");
	System.out.println(gondola+" gondola cars");
	System.out.println(passenger+" passenger cars");
	System.out.println("The total weight of the of the cars is "+ totalweightofcars +" tons.");
	System.out.println("The number of engines required is "+exacteng+".");
	System.out.println("The total weight of the entire train is "+totalweightoftrain+" tons.");
	System.out.println("The total train is "+totallengthoftrain+" feet long.");
	keyboard.close();
    }

    }
