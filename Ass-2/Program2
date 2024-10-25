# Superclass representing a generic vehicle
class Vehicle
  attr_accessor :fuel_level, :mileage

  def initialize(fuel_level, mileage)
    @fuel_level = fuel_level
    @mileage = mileage
  end

  # Method to check the fuel level
  def check_fuel
    puts "Fuel level: #{@fuel_level} liters."
  end

  # Method to calculate mileage
  def calculate_mileage(distance, fuel_used)
    @mileage = distance / fuel_used
    puts "Mileage: #{@mileage} km per liter."
  end

  # Method to perform general maintenance
  def perform_maintenance
    puts "Performing general vehicle maintenance."
  end
end

# Subclass representing a car
class Car < Vehicle
  attr_accessor :trunk_capacity

  def initialize(fuel_level, mileage, trunk_capacity)
    super(fuel_level, mileage)  # Call the parent class's initializer
    @trunk_capacity = trunk_capacity
  end

  # Specific method for the car class
  def open_trunk
    puts "Opening the car trunk. Capacity: #{@trunk_capacity} liters."
  end
end

# Subclass representing a truck
class Truck < Vehicle
  attr_accessor :cargo_capacity

  def initialize(fuel_level, mileage, cargo_capacity)
    super(fuel_level, mileage)
    @cargo_capacity = cargo_capacity
  end

  # Specific method for the truck class
  def load_cargo(weight)
    puts "Loading cargo. Current load: #{weight} kg out of #{@cargo_capacity} kg capacity."
  end
end

# Subclass representing a motorcycle
class Motorcycle < Vehicle
  attr_accessor :helmet_type

  def initialize(fuel_level, mileage, helmet_type)
    super(fuel_level, mileage)
    @helmet_type = helmet_type
  end

  # Specific method for the motorcycle class
  def wear_helmet
    puts "Wearing a #{@helmet_type} helmet."
  end
end

# Example usage:
car = Car.new(50, 15, 500)
car.check_fuel             # Inherited from Vehicle class
car.calculate_mileage(300, 20)  # Inherited from Vehicle class
car.open_trunk             # Specific to Car class

truck = Truck.new(100, 10, 3000)
truck.load_cargo(2000)      # Specific to Truck class

motorcycle = Motorcycle.new(10, 40, "full-face")
motorcycle.wear_helmet      # Specific to Motorcycle class
