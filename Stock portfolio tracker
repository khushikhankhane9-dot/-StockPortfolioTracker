
prices = {
    "AAPL": 180,
    "TSLA": 250,
    "GOOGL": 140
}

total = 0
portfolio = []

while True:
    stock = input("Enter stock name (or 'done' to finish): ").upper()

    if stock == "DONE":
        break

    if stock not in prices:
        print("Stock not found. Please try again.")
        continue

    quantity = int(input("Enter quantity: "))

    price = prices[stock]
    value = price * quantity
    total += value

    portfolio.append(
        f"{stock}: {quantity} x {price} = {value}"
    )

print("\nYour Stock Portfolio")

for item in portfolio:
    print(item)

print("Total investment:", total)

save = input("Do you want to save the portfolio? (yes/no): ").lower()

if save == "yes":
    file = open("portfolio.txt", "w")

    for item in portfolio:
        file.write(item + "\n")

    file.write("Total investment: " + str(total))
    file.close()

    print("Portfolio saved successfully!")
