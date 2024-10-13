# 8. View order list
def showOrders():
    if not orderlist:
        print("No orders found.")
        return

    print("----------Order Information----------")
    print("-Order ID----Username----Total Price----Order Status-")
    for order in orderlist:
        print(f"-{order['order_id']}----{order['username']}----{order['total_price']:.2f}----{order['order_status']}")
    print("----------------------------")

# 9. View order details
def showOrderDetails():
    order_id = input("Please enter the order ID to view: ")

    # Check if the order exists
    for order in orderlist:
        if order["order_id"] == order_id:
            print("----------Order Details----------")
            print(f"Order ID: {order['order_id']}")
            print(f"Username: {order['username']}")
            print(f"Total Price: {order['total_price']:.2f}")
            print(f"Order Status: {order['order_status']}")
            print("Product List:")
            for item in order["product_list"]:
                for product in commoditylist:
                    if product["id"] == item["id"]:
                        print(f"  {product['name']} x {item['quantity']}")
                        break
            print("----------------------------")
            return

    # If order ID not found
    print("Order number does not exist, please re-enter.")
