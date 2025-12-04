# CS2-Project-Q2
Code: 
print("=== SCHOOL LUNCH PRICE CALCULATOR ===")

prices = []

while True:
    print("\n1. Add item price")
    print("2. View prices")
    print("3. Calculate total")
    print("4. Exit")

    choice = input("Choose: ")

    if choice == "1":
        price = float(input("Enter item price: "))
        prices.append(price)
        print("Added!")

    elif choice == "2":
        if len(prices) == 0:
            print("No items yet!")
        else:
            print("Items you added:")
            for i in range(len(prices)):
                print(f"{i+1}. ₱{prices[i]}")

    elif choice == "3":
        total = sum(prices)
        print(f"Total cost: ₱{total}")

    elif choice == "4":
        print("See you next time!")
        break

    else:
        print("Invalid choice.")
