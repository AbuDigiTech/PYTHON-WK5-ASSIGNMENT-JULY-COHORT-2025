class Vehicle:
    def __init__(self, brand, model, year):
        self.brand = brand
        self.model = model
        self.year = year
        self.mileage = 0

    def drive(self, miles):
        self.mileage += miles

    def describe_vehicle(self):
        print(f"This vehicle is a {self.year} {self.brand} {self.model} with {self.mileage} miles.")

class Car(Vehicle):
    def __init__(self, brand, model, year, doors):
        super().__init__(brand, model, year)
        self.doors = doors

    def describe_vehicle(self):
        super().describe_vehicle()
        print(f"It has {self.doors} doors.")

    def drive(self, miles):
        super().drive(miles)
        print(f"The car has been driven for {miles} miles.")

class Truck(Vehicle):
    def __init__(self, brand, model, year, capacity):
        super().__init__(brand, model, year)
        self.capacity = capacity

    def describe_vehicle(self):
        super().describe_vehicle()
        print(f"It has a capacity of {self.capacity} tons.")

    def drive(self, miles):
        super().drive(miles)
        print(f"The truck has been driven for {miles} miles.")

# Create objects
my_car = Car('Toyota', 'Corolla', 2015, 4)
my_truck = Truck('Ford', 'F-150', 2020, 2)

# Use methods
my_car.drive(100)
my_car.describe_vehicle()

my_truck.drive(50)
my_truck.describe_vehicle()
