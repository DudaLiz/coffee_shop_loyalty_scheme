class Customer:
    def __init__(self, name):
        self.name = name
        self.stamps = 0
        self.points = 0

    def buy_coffee(self):
        self.stamps += 1
        if self.stamps % 8 == 0:
            print("Congratulations! You've earned a free coffee!")

    def buy_food(self, quantity):
        self.points += quantity * 5

    def view_rewards(self):
        print(f"{self.name}'s Rewards:")
        print(f"Stamps: {self.stamps}")
        print(f"Points: {self.points}")

class CoffeeShop:
    def __init__(self):
        self.customers = {}

    def add_customer(self, customer):
        self.customers[customer.name] = customer

    def process_order(self, customer_name, item, quantity=1):
        if item == "coffee":
            self.customers[customer_name].buy_coffee()
        elif item == "food":
            self.customers[customer_name].buy_food(quantity)
        else:
            print("Invalid item.")

        # Send order to coffee shop (dummy implementation)
        print(f"Order received from {customer_name}: {quantity} {item}(s)")

# Example usage:
coffee_shop = CoffeeShop()

# Adding customers
customer1 = Customer("Alice")
customer2 = Customer("Bob")
coffee_shop.add_customer(customer1)
coffee_shop.add_customer(customer2)

# Process orders
coffee_shop.process_order("Alice", "coffee")
coffee_shop.process_order("Alice", "food", 2)
coffee_shop.process_order("Bob", "coffee")
coffee_shop.process_order("Bob", "food")

# View rewards
customer1.view_rewards()
customer2.view_rewards()
