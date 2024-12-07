// Vehicle.java
public class Vehicle {
    private String model;
    private int year;

    // Constructor
    public Vehicle(String model, int year) {
        this.model = model;
        this.year = year;
    }

    // Getter and Setter
    public String getModel() {
        return model;
    }

    public void setModel(String model) {
        this.model = model;
    }

    public int getYear() {
        return year;
    }

    public void setYear(int year) {
        this.year = year;
    }

    // Method to show information
    public void showInfo() {
        System.out.println("Model: " + model + ", Year: " + year);
    }
}

// Car.java
public class Car extends Vehicle {
    private int numberOfDoors;

    // Constructor
    public Car(String model, int year, int numberOfDoors) {
        super(model, year);
        this.numberOfDoors = numberOfDoors;
    }

    // Getter and Setter
    public int getNumberOfDoors() {
        return numberOfDoors;
    }

    public void setNumberOfDoors(int numberOfDoors) {
        this.numberOfDoors = numberOfDoors;
    }

    // Override showInfo method
    @Override
    public void showInfo() {
        super.showInfo();
        System.out.println("Number of Doors: " + numberOfDoors);
    }
}

// Bike.java
public class Bike extends Vehicle {
    private boolean hasCarrier;

    // Constructor
    public Bike(String model, int year, boolean hasCarrier) {
        super(model, year);
        this.hasCarrier = hasCarrier;
    }

    // Getter and Setter
    public boolean isHasCarrier() {
        return hasCarrier;
    }

    public void setHasCarrier(boolean hasCarrier) {
        this.hasCarrier = hasCarrier;
    }

    // Override showInfo method
    @Override
    public void showInfo() {
        super.showInfo();
        System.out.println("Has Carrier: " + hasCarrier);
    }
}

// Main.java
public class Main {
    public static void main(String[] args) {
        Car car = new Car("Toyota Corolla", 2020, 4);
        Bike bike = new Bike("Yamaha", 2018, true);

        System.out.println("Car Information:");
        car.showInfo();

        System.out.println("\nBike Information:");
        bike.showInfo();
    }
}
