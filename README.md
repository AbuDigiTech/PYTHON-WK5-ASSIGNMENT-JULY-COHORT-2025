class Animal:
    def __init__(self, name):
        self.name = name

    def move(self):
        pass

class Dog(Animal):
    def move(self):
        print(f"{self.name} the dog is running.")

class Bird(Animal):
    def move(self):
        print(f"{self.name} the bird is flying.")

class Fish(Animal):
    def move(self):
        print(f"{self.name} the fish is swimming.")

# Create objects
my_dog = Dog('Buddy')
my_bird = Bird('Tweety')
my_fish = Fish('Goldie')

# Use polymorphism
animals = [my_dog, my_bird, my_fish]
for animal in animals:
    animal.move()
