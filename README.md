# BongoBD-Test
# Bongo's Frontend Developer Position Assigment

## Problem Anagram:

**Write a function that detects if two strings are an anagram e.g. ‘bleat’ and ‘table’ are anagrams but ‘eat’ and ‘tar’ are not.**

[Code Snippet](https://github.com/mousumi-biswas/BongoBD-Test/tree/master/anagaram)

## Problem Design Pattern:

**Explain the design pattern used in following:**

interface Vehicle {
int set_num_of_wheels()
int set_num_of_passengers()
boolean has_gas() 
}


**Ans:** 

It is interface, not a specific pattern. The interface can be used in a design pattern however, such as the Factory Pattern, Builder, or Adapter Pattern, etc.

**Explain how can you use the pattern to create car and plane class?**

**Ans:**

To create a "Car" or "Plane", you would simply implement the interface in a concrete class, and return the appropriate values for each function. If a factory pattern, the factory would simply return an implementation of some sort that implemented that interface.

      
      class VehicleFactory {
        public Vehicle create(int type) {
            if(type == 0){ 
                 return new Car();
            }
            return new Plane();
        }
      }

      class Car implements Vehicle {
          int set_num_of_wheels(){return 4}
          int set_num_of_passengers() {return 5}
          boolean has_gas() {return true}
      }
      
      class Plane implements Vehicle {
          int set_num_of_wheels(){return 5}
          int set_num_of_passengers() {return 200}
          boolean has_gas() {return true}
      }


**Use a different design pattern for this solution**

    Using Builder Pattern:
    class VehicleBuilder {
         int num_of_wheels = 0;
        int num_of_passengers = 0;
        boolean has_gas = false;

     public VehicleBuilder wheels(int wheels) {
         num_of_wheels = wheels
         return this;
     }

     public VehicleBuilder passengers(int passengers) {
         num_of_passengers = passengers
         return this;
     }

     public VehicleBuilder gas(boolean gas) {
         has_gas = gas
         return this;
     }

    public Vehicle build() {
         return new VehicleImpl(num_of_wheels, num_of_passengers, has_gas);
        
    }
    }
    class VehicleImpl(int wheels, int passengers,boolean gas) implements Vehicle {
      int set_num_of_wheels(){return wheels}
      int set_num_of_passengers() {return passengers}
      boolean has_gas() {return gas}
   }
   
  ## Problem Video Player:
  
  [CodeSnippet](https://github.com/mousumi-biswas/BongoBD-Test/tree/master/video-player)
