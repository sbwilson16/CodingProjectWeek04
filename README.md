"# CodingProjectWeek04"
package week03;

public class CodingProjectWeek04 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
//Create an array of int called ages that contains the following values: 3, 9, 23, 64, 2, 8, 28, 93.
		
		int[] age = {3 ,9, 23, 64, 2, 8, 28, 93}; 
		// You want to make sure you use the [] brackets after int to make it an array.
		
//
//a. Programmatically subtract the value of the first element in the array from the value in the last element of the array (i.e. do not use ages[7] in your code). Print the result to the console.  
//
		System.out.println( age[0] - age[age.length - 1]);
		// The array starts with 0 place holder and then you want to use the age.length - 1 to subtract the last number in the array.
		
//b. Create a new array of int called ages2 with 9 elements (ages2 will be longer than the ages array, and have more elements).  
	int[] age2 = {47,2,9,65,34,77,26,8,15}; // the new array has 9 elements. 0 is equal to 47 and 8 is 15. So 47 - 15 = 32.
		
		
//i. Make sure that there are 9 elements of type int in this new array.  
//
//ii. Repeat the subtraction from Step 1.a. (Programmatically subtract the value of the first element in the new array ages2 from the last element of ages2). 
//
	System.out.println(age2[0] - age2[age.length - 1]); // the first element is equal to 0 and the last element will be the length of the array - 1
	
//iii. Show that using the index values for the elements is dynamic (works for arrays of different lengths).
//
//c. Use a loop to iterate through the array and calculate the average age. Print the result to the console.
//
	int sum = 0; //made a sum to 0 
	for ( int average : age2) { //make a new index in age2 
		sum += average; // deculation of sum in the for loop 
	}
	int average2 = sum / age2.length; //divide the sum to the age array using the .length. declare a new varible 
	System.out.println(average2); // print the average 
	
	
//2. Create an array of String called names that contains the following values: “Sam”, “Tommy”, “Tim”, “Sally”, “Buck”, “Bob”.
//
	String[] names = {"Sam", "Tommy", "Tim", "Sally", "Buck", "Bob"}; // to make an array use []
//a. Use a loop to iterate through the array and calculate the average number of letters per name. Print the result to the console.
//  
	int averageLetters = 0; 
	for ( String length : names) { // i fallowed the same methond as qustion 1. 
		averageLetters += length.length(); // however since it is a string i put a .length.
	}
	    int averageLetter = averageLetters / names.length; 
	    System.out.println(averageLetter);
	
//b. Use a loop to iterate through the array again and concatenate all the names together, separated by spaces, and print the result to the console.
//
	//String[] names = {"Sam", "Tommy", "Tim", "Sally", "Buck", "Bob"}; 
    String students = "";

for (int i = 0; i < names.length; i++) {
    	 
    	students += names[i] + " ";
     
   } 
	  System.out.println(students);
//3. How do you access the last element of any array?
//use array.length - 1 to access the last element of any array.
	System.out.println(names[names.length - 1]);
//4. How do you access the first element of any array?
//use 0 to access the first element of any array
	System.out.println(names[0]);
//5. Create a new array of int called nameLengths. Write a loop to iterate over the previously created names array and add the length of each name to the nameLengths array.
  int nameLength = 0; //create new varible 
	for(String name : names) {  // for each name in names
		nameLength += name.length(); // set the new variable += to name.length
	} System.out.println(nameLength);
//6. Write a loop to iterate over the nameLengths array and calculate the sum of all the elements in the array. Print the result to the console.
//
         int count = 0; 
	 for(int i = 0; i < names.length; i++)
	 {
		 count += names.length; 
	 } System.out.println(count);
       

	} // end of main *********
	//7. Write a method that takes a String, word, and an int, n, as arguments and returns the word concatenated to itself n number of times. (i.e. if I pass in “Hello” and 3, I expect the method to return “HelloHelloHello”).
	//
	static String repeatWord(String word, int n) {
		String newWord = "";   //make a new variable 
		for(int i = 0; i < n; i++) { // Make a for loop to tell the loop how much to repeat the word
			newWord += word;
		}  
		
		return newWord; // return to the new variable to the method
	}
	    
	
	//8. Write a method that takes two Strings, firstName and lastName, and returns a full name (the full name should be the first and the last name as a String separated by a space).
	//
	     static void userName( String fullName ) { // using viod since i am not returing any data 
	    	String firstName = "Ally";
	    	String lastName = "Ramirez";
	    	System.out.println(firstName + " " + lastName);
	    
	     }
	
	//9. Write a method that takes an array of int and returns true if the sum of all the ints in the array is greater than 100.
	//
	      public boolean groupOfNumbers(int sum1) {
	    	  int[] groupsOfNumbers = { 5, 2, 15, 75, 39, 22,};  
	    	for(int i = 0; i < groupsOfNumbers.length; i++) { // add the sum of all elements
	    		sum1 += groupsOfNumbers[i]; // find the sum of the elements 
	    		
	    	}
			if( sum1 > 100) { // create an if statement to see if the numbers are greater than 100
				return true; // return statement if true. 
			
			} else { return false; // use the else statement to return false
				
			}
	      }
			
	//10. Write a method that takes an array of double and returns the average of all the elements in the array.
	//
	        public double numberList() { // use a double method 
	    	  double[] numberList = { 2.30, 1.92, 45.80, 7.98}; 
	    	double averg = 0;
	    	  for(double numberOfList : numberList) {
	    		 averg += numberOfList; 
	    		  
	      } return averg / numberList.length; // return to the method 
	      
	      }
	//11. Write a method that takes two arrays of double and returns true if the average of the elements in the first array is greater than the average of the elements in the second array.
	//
	        public boolean groupsOfNumber(double twoArrays1, double numberList1) { // made the method a boolean and add the two double elemnts that would be in the proplem 
	        	double[] twoArrays = { 1.80, 66.0, 5.95, 12.75}; 
	        	double secondArray = 0;  
	        	for(double sums : twoArrays) {
	        			secondArray += sums;
	        	} double avg = (secondArray / twoArrays.length); // here i found the adverge of the first array 
	        	
	        	  double[] numberList = { 2.30, 1.92, 45.80, 7.98}; // i did the same thing for the second array 
	     	    	double averg = 0;
	     	    	  for(double numberOfList : numberList) {
	     	    		  averg += numberOfList;
	     	    	  } double avg2 = (averg / numberList.length);
	        		
	        		 if (avg > avg2) { // i wrote an if statement so that i can do a return for true and false.
	        			 return true; 
	        		 }
					return false;
	        
	        	
	        }
	//12. Write a method called willBuyDrink that takes a boolean isHotOutside, and a double moneyInPocket, and returns true if it is hot outside and if moneyInPocket is greater than 10.50.
	//
	        public static boolean willBuyDrink( boolean isHotOutside, double moneyInPocket) {
	        	if (isHotOutside = true && moneyInPocket > 10.50) { // did an if statement 
	        		return true;
	        	} else {
	        		 return false;
	        		
	        	  }
	        }
	        
	      //13. Create a method of your own that solves a problem. In comments, write what the method does and why you created it.
          // i created a method that can help you find out if you have enough money to go on vacation. it adds the money that you set aside and
	        // adds the total money saved to see if you can afford Paris. 
                          public  void vacationToParis (String canWeAfford, int moneySaved) {
                      
                         int[] moneySetAside = { 946, 874, 463, 536,}; 
                        	 int moneySaved1 = 0;
                        	
                        	 for (int i = 0; i < moneySetAside.length; i++) {
                        		  moneySaved1 += moneySetAside[i]; 
                        	  } if (moneySaved1 > 4000) {
                        		  System.out.println("Lets go to Paris!");
                        	  } else {
                        		  System.out.println("We will have to save up more money.");
                        	  }





}

}









