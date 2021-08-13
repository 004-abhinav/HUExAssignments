package automation;

import java.util.ArrayList;
import java.util.HashMap;

public class OOPsAssignment {
	
	public String str1;
	
	public static void checkPalindrome(String str1) {
		String reversedString = new StringBuilder(str1).reverse().toString();
	//	System.out.println(reversedString);
		if (str1.equals(reversedString)) {
			System.out.println("The given string is a palindrome.");
		}
		else{
			System.out.println("The given string is not a palindrome.");
		}
	}
	
	public static void probablePalindrome(String str1) {
	    {	  
	        HashMap<Character, Integer> charCount = new HashMap<Character, Integer>();
	    
	        char[] strArray = str1.toCharArray();
	        for (char c : strArray)
	        {
	            if(charCount.containsKey(c))
	            {
	                charCount.put(c, charCount.get(c)+1);
	            }
	            else
	            {
	                charCount.put(c, 1);
	            }
	        }
	       // System.out.println(str1+" : "+charCount);
	        
	        ArrayList<Integer> arrayList = new ArrayList<Integer>();  
	        arrayList.addAll(charCount.values()); 
	        
	    //    System.out.println(arrayList);
	        int oddCount = 0;
	        for (int i=0;  i  < arrayList.size(); i++)
	        {
	        	if (arrayList.get(i)%2!=0)
	        		oddCount=oddCount+1;
	        }
	        
	        if (oddCount>1) {
	        	System.out.println("The given string cannot be converted into palindrome");
	        }
	        else
	        	System.out.println("The given string can be converted into palindrome");
	    }
	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		OOPsAssignment.checkPalindrome("nitin");
		OOPsAssignment.probablePalindrome("hashedinbydeloitte");
	}

}
