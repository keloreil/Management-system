# 10. Show available products
def showProduct():
    print("----------Available Products----------")
    print("-Product ID----Product Name----Price----Discount-")
    for product in commoditylist:
        print(f"-{product['id']}----{product['name']}----{product['price']:.2f}----{product['discount'] * 100}%")
    print("----------------------------")

# Main Menu
def mainMenu():
    while True:
        print("\n----------Main Menu----------")
        print("1. Create a new order")
        print("2. View orders")
        print("3. View order details")
        print("4. Exit")
        choice = input("Please choose an option (1/2/3/4): ")

        if choice == "1":
            createOrder()
        elif choice == "2":
            showOrders()
        elif choice == "3":
            showOrderDetails()
        elif choice == "4":
            print("Exiting the program. Goodbye!")
            break
        else:
            print("Invalid option. Please try again.")
