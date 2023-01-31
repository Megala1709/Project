# Projectimport java.util.*;
//import java.util.LinkedHashMap;
//import java.util.LinkedHashSet;


public class Main {
   
	public static void main(String[] args) 
	{
		// TODO Auto-generated method stub
		 HashMap<String, Integer> medicinemap = new LinkedHashMap<String, Integer>();
		
		 System.out.println("             Login to the System          ");
		 Scanner scanner=new Scanner(System.in);
		 System.out.print("UserName: ");
		 String username=scanner.next();
		 System.out.print("Password: ");
		 String password=scanner.next();
		
		 if(username.equals("medicalstocks")&&password.equals("nkm1709"))
		 {
         System.out.println("               WELCOME TO NKM MEDICALS    ");
         System.out.println("1.Medicines Details");
         System.out.println("2.Sales Details");
         System.out.println("3.Import Details");
         System.out.println("4.Medicines Availability");
         System.out.print("Enter Your Option To View Details: ");
         int operation=scanner.nextInt();
         if(operation<=4)
         {
         switch(operation)
         {
         case 1:
        	    System.out.println("             Enter the option to view medicine  details");
        	    System.out.println("1.Medicine list\n"+"2.Search Medicine\n"+"3.Add Medicine\n"+"4.Delete Medicine");
        	    int medicineop=scanner.nextInt();
        	    switch(medicineop)
        	    {
        	    case 1:
        	    	
        	    	break;
        	    case 2:
        	    	 searchmedicine(medicinemap);
        	    	break;
        	    case 3:
        	    	HashMap<String, Medicine> addmedicine = addmedicine();
        	    	 break;
        	    case 4:
        	    	  deletemedicine(medicinemap);
        	    	break;
        	 }
        	
        	
              break;
         case 2:
        	 System.out.println("hii"); 
        	 break;
  
         case 3:
        	 System.out.println("hii");
        	 break;
         case 4:
        	 System.out.println("hii");
        	 break;
         }
		 }
         else
         {
        	 System.out.println("Invalid operation \n Enter 1 to 4 to continue the operation");
         }
		 }
		 else
		 {
			 System.out.println("Ivalid Username or Password");
		 }
	
		}
	 private static void deletemedicine(HashMap<String, Integer> medicinemap) {
		// TODO Auto-generated method stub
		
	}
	private static void searchmedicine(HashMap<String,Integer> medicinemap)
	 {  
		/*Scanner scanner=new Scanner(System.in);
		System.out.println("Enter The Medicine Name To Be Searched");
		String medicinename1=scanner.nextLine();
		if(medicinename1.equals(medicinemap.medicinename))
		{
			
		for()*/
	 }
	
	public static void addmedicine(HashMap<String , Medicine > medicinemap)
	 {
		System.out.println("Enter Medition Details to be added ");
		Scanner scanner=new Scanner(System.in);
		
		System.out.print("Enter the Medicine Name");
		String medicinename=scanner.nextLine();
        
		System.out.println("Enter Strength of the medicine");
		int strength=scanner.nextInt();
		
		System.out.println("Enter Quantity of the medicine");
		int quantity=scanner.nextInt();
		
		System.out.println("Enter price of the medicine");
		float price=scanner.nextFloat();
		
		System.out.println("Enter purchase of the medicine");
		String purchasedate=scanner.nextLine();
		
		System.out.println("Enter Expirey of the medicine");
		String expireydate=scanner.nextLine();
		
		medicinemap.put(medicinename, new Medicine(medicinename, strength,quantity,price,purchasedate,expireydate));
        System.out.println("Medicine Details added Successfully");
		// return medicinelist
	 }

}
