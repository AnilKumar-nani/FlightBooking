# FlightBooking
The requirement is to book flight ticket, so that i took 4 classes 
To get detailes from the user or to register i used a class named UserDetailes.java

     public UserDetails(String name, String mobNum, String govId, String dob, String email, String password) {
      super();
      this.name = name;
      this.mobileNumber = mobNum;
      this.govId = govId;
      this.dob = dob;
      this.emailId = email;
      this.password = password;
    } 
with help of this class user is able to provide his detailes to register 

after to get the detailes of from and to, to where the user wish to fly i used another class Travels.java

      public Travels(String name, String age, String flightName, String from, String to, String startTime, String endTime,
			String price) {
		super();
		this.name = name;
		this.age = age;
		this.flightName = flightName;
		this.from = from;
		this.to = to;
		this.startTime = startTime;
		this.endTime = endTime;
		this.price = price;
	}
 with the help of this class user is able to select the to and from of the flights 
 
 
and to slectt the flights

     public String toString() {
			return "ListOfFlights [flightName=" + flightName + ", from=" + from + ", to=" + to + ", startTime=" + startTime
					+ ", endTime=" + endTime + ", price=" + price + "]";
		}

and the main class which contains all the is UserInterface

public static boolean verityInfoOfNewRegister(List<UserDetails> user,String phNum) {
		
		for(UserDetails d:user) {
			if(d.getMobNum().equals(phNum)) return false;
		}
		return true;
		
		
	}
to login with the credentials we can use this 

     try {
			System.out.println("enter name:");
			name = br.readLine();
			System.out.println("enter age:");
			age = br.readLine();
			flightName = flight.getFlightName();
			from = flight.getFrom();
			to = flight.getTo();
			startTime = flight.getStartTime();
			endTime = flight.getEndTime();
			price = flight.getPrice();
			Travels journey = new Travels(name, age, flightName, from, to, startTime, endTime, price);
			System.out.println("booking your ticket...");
			try {
				Thread.sleep(1000);
				System.out.println("ticket booked successfully...!\n");
we can book ticket with this

for regeistering purpose 

      String name,mobNum,govId,dob,email,password;
		try {
			
			System.out.println("enter name:");
			name = br.readLine();
			System.out.println("enter mobilenumber:");
			mobNum = br.readLine();
			System.out.println("enter govidNum:");
			govId = br.readLine();
			System.out.println("enter dob(DD/MM/YYYY):");
			dob = br.readLine();
			System.out.println("enter emailId:");
			email = br.readLine();
			System.out.println("enter Password:");
			password = br.readLine();
			
      
     public static void main(String[] args) {
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		
		List<UserDetails> userInfo = new ArrayList<>();
		
		List<AllFlights> allFlights = new ArrayList<>();  
		
		allFlights.add(new AllFlights("Indigo","hyderabad","vijayawada","1:00pm","4:30pm","3499"));
		allFlights.add(new AllFlights("Redbus","hyderabad","mumbai","13:00","24:00","9900"));
		allFlights.add(new AllFlights("KingFisher","chennai","mumbai","8:40","3:20","2000"));
		allFlights.add(new AllFlights("Versa","bangalore","hyderabad","19:45","23:50","35500"));
		allFlights.add(new AllFlights("Truejet","andaman","srilanka","22:25","12:50","100000"));
		allFlights.add(new AllFlights("GoInia","Chennai","hyderabad","4:00","10:30","3800"));
		allFlights.add(new AllFlights("kingfisher","hyderabad","goa","15:20","23:40","10000"));
    
user can select the flight from thses list 

    do {
          System.out.println("\n1.Register\n2.Login\n3.Exit");
          try {
            choice = Integer.parseInt(br.readLine());
          } catch (NumberFormatException | IOException e) {
            System.out.println("Invalid entry\nenter valid choice..");
            continue;
          }
user faces a selection among register, login and exit 

    case 1: {
				
				UserDetails adding = userRegistration(userInfo);
				if(adding != null) {
					userInfo.add(adding);
				}
with help of user detailes class he will able to register 

    case 2: {
				String mobNum,password;
				try {
					System.out.println("Enter MobileNumber:");
					mobNum = br.readLine();
					System.out.println("Enter Password:");
					password = br.readLine();
					int index = loginUser(userInfo,mobNum,password);
					if(index != -1) 
  to login 
          int userChoice = 0;
						do {
							System.out.println("\n1.BookTicket\n2.History\n3.Exit");
							try {
								userChoice = Integer.parseInt(br.readLine());
                
  after login he have to select among these choices
  
  if he press to book ticket he have to fill the detailes 
  
      case 1: {
									int i=1;
										String from,to;
										System.out.println("From...");
										from = br.readLine().toLowerCase();
										System.out.println("To");
										to = br.readLine().toLowerCase();
										boolean noFlight = true;
										List<AllFlights> availbleFlights = new ArrayList<>();
									for(AllFlights list:allFlights) {
										if(list.getFrom().equals(from) && list.getTo().equals(to)) {
											System.out.println(i++ +"-->"+ list);
											availbleFlights.add(list);
											noFlight = false;
										}
 if there are no flights between his route it will diplay 
 
          if(noFlight) {
										System.out.println("no flights found in the route?");
										continue;
									}
  after booking he is able to see his history of bookings and finally exit.
  
