# Fleet-Management-System
This is a code with Java script. This will be helped to managed the vehicle systems like fuel efficiency and maintain requirements. 
class Vehicle {  
    private String id;  
    private double mileage;  
    private double fuel;  
   
    public Vehicle(String id, double mileage, double fuel) {  
     this.id = id;  
     this.mileage = mileage;  
     this.fuel = fuel;  
    }  
    public void drive(double distance) { 
     if (fuel > 0) {  
       mileage += distance;  
       fuel -= distance / 10; // Simple fuel consumption  
     }  
    }  
    public boolean needsMaintenance() {  
     return mileage >= 10000;  
    }  
    public void displayStatus() {  
     System.out.println("Vehicle " + id + ":");  
     System.out.println("Mileage: " + mileage + " km");  
     System.out.println("Fuel: " + fuel + " L");  
  if (needsMaintenance()) {  
  System.out.println("Maintenance Required!");  
  }  
  }  
  }  
  class FleetManagementSystem {  
  public static void main(String[] args) {  
  Vehicle truck = new Vehicle("T001", 9500, 100);  
  Vehicle car = new Vehicle("C001", 8000, 50);  
  truck.drive(600);  
  car.drive(400);  
  truck.displayStatus();  
  System.out.println();  
  car.displayStatus();  
  }  
  } 
