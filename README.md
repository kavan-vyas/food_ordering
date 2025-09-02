# Food Ordering System

A console-based food ordering system built in Python that allows users to browse menus, place orders, and process payments with automatic discount calculations.

## Features

- **Menu Management**: Browse foods, drinks, and additional services
- **Order Processing**: Add items to cart with quantity selection
- **Payment System**: Calculate totals with tiered discount system
- **Receipt Generation**: Generate and store transaction reports
- **Cross-Platform**: Works on Windows and Unix-based systems

## Discount Structure

The system applies automatic discounts based on order total:
- **5% discount** for orders over $200
- **10% discount** for orders over $1,000  
- **15% discount** for orders over $5,000

## File Structure

```
food_ordering/
├── index.py           # Main application file
├── files/
│   ├── list_foods.fsd    # Food menu items and prices
│   ├── list_drinks.fsd   # Drink menu items and prices
│   ├── list_services.fsd # Additional services and prices
│   └── report.fsd        # Transaction history storage
└── README.md
```

## Data Format

Menu items in the `.fsd` files should follow this format:
```
Item Name $ Price
```
Example:
```
Pizza $ 12.99
Burger $ 8.50
```

## How to Run

1. Ensure Python is installed on your system
2. Navigate to the project directory
3. Run the application:
   ```bash
   python index.py
   ```

## Usage

### Main Menu Options:
- **(O) ORDER** - Browse and order items
- **(R) REPORT** - View transaction history
- **(P) PAYMENT** - Process current order and payment
- **(E) EXIT** - Exit the application

### Order Menu Options:
- **(F) FOODS AND DRINKS** - Browse food and drink menus
- **(O) OTHER SERVICES** - Browse additional services
- **(M) MAIN MENU** - Return to main menu
- **(E) EXIT** - Exit the application

### Ordering Process:
1. Select items by entering their number
2. Specify quantity when prompted
3. Continue adding items or proceed to payment
4. Review order total and applicable discounts
5. Complete payment to generate receipt

## System Requirements

- Python 3.x
- Standard Python libraries (os, datetime)

## Notes

- The system automatically sorts menu items alphabetically
- Transaction reports are timestamped and stored persistently
- Cross-platform file path handling for Windows and Unix systems
- Input validation prevents invalid selections and quantities

## Contributing

To add new menu items:
1. Edit the appropriate `.fsd` file in the `files/` directory
2. Follow the format: `Item Name $ Price`
3. Restart the application to load new items