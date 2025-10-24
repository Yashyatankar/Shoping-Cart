addToCart = str(input('Add to cart? yes/no: '))
cart = []
prices = []
total = 0.0

while True:
    
    if addToCart == 'no':
        print('Thank you for shopping with us!')
        break
    else:
        cart.append(str(input('Enter item to add to cart or q to quit: ')))
        prices.append(float(input('Enter price of the item: ')))
        if cart[-1] == 'q':
            cart.pop()
            prices.pop()
            print('Thank you for shopping with us!')
            break
    
for price in prices:
    total += price
    print(f'Item price: ${price:.2f}')
print(f'Total price: ${total:.2f}')
