# 7. Create a new order
def createOrder():
    showProduct()
    order_items = []
    total_price = 0.0

    while True:
        product_id = input("Please enter the product ID to purchase (enter 0 to finish): ")
        if product_id == "0":
            break
        quantity = input("Please enter the quantity to purchase: ")

        # Check if the quantity is a valid integer
        try:
            quantity = int(quantity)
            if quantity <= 0:
                print("Invalid quantity. Quantity should be a positive number.")
                continue
        except ValueError:
            print("Invalid input. Please enter a valid number for quantity.")
            continue

        # Find the product in the commodity list
        for product in commoditylist:
            if product["id"] == product_id:
                item_price = product["price"] * product["discount"] * quantity
                total_price += item_price
                order_items.append({"id": product_id, "quantity": quantity})
                print(f"Added {product['name']} x {quantity} to the order, total price for this item: {item_price:.2f}")
                break
        else:
            print("Product ID does not exist, please try again.")

    if order_items:
        order_id = str(len(orderlist) + 1).zfill(3)  # Generate order ID
        new_order = {
            "order_id": order_id,
            "username": "111",  # Assume current user is "111", modify as needed
            "product_list": order_items,
            "total_price": total_price,
            "order_status": "Ordered"
        }
        orderlist.append(new_order)
        print(f"Order created successfully! Order ID: {order_id}, Total Price: {total_price:.2f}")
    else:
        print("The order is empty, no order created.")
