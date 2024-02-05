# Checklist MT4 - Trading Robot

This code is a trading robot developed by Forex Robot Easy Team. It is designed to streamline trading by providing an on-screen checklist of trades. The checklist keeps track of open trades, their details, and allows the user to close trades directly from the checklist.

## How It Works
1. The code includes the necessary libraries, such as `Trade` and `Button`, which provide functionality for trading and creating buttons on the MetaTrader 4 platform.
2. Constants are defined to specify the column positions in the checklist display.
3. Global variables are declared, including an instance of `CTrade` for trading operations, a variable to store the total number of rows in the checklist, and a 2-dimensional array `checklist` to store trade details.
4. The `InitializeChecklist()` function initializes the checklist by setting the total number of rows to 0.
5. The `AddTradeToChecklist()` function adds a new trade to the checklist. It takes parameters such as ticket number, symbol, trade type, and lots. It checks if there is enough space in the checklist array and then adds the trade details to the checklist array.
6. The `CloseTradeInChecklist()` function closes a trade in the checklist. It takes parameters such as ticket number, close price, and profit. It iterates through the checklist array to find the trade with the given ticket number and updates the close price, profit, and status of the trade.
7. The `UpdateChecklistDisplay()` function updates the checklist display on the screen. It clears the existing display and then iterates through the checklist array to display the trade details in the appropriate cells on the screen.
8. The `OnButtonClick()` function handles button clicks on the checklist. In this code, it is specifically designed to handle the click event of a 'Close Trade' button. It retrieves the selected row from the checklist, gets the ticket number of the trade, asks the user for the close price and calculates the profit, and then calls the `PositionClose()` function of the `CTrade` instance to close the trade. Finally, it updates the checklist display.
9. The `OnInit()` function is the entry point of the program. It initializes the checklist and creates the checklist display on the screen. It also creates a 'Close Trade' button and assigns the `OnButtonClick()` function as its click event handler.
10. The `OnTick()` function is the main loop of the program. It periodically updates the checklist display every minute.
11. The `OnDeinit()` function is the exit point of the program. It is used to clean up any resources used by the program.

## Product Description

Checklist MT4 is a trading robot developed by Forex Robot Easy Team. It provides traders with an on-screen checklist to streamline their trading process. With Checklist MT4, traders can easily keep track of their open trades, view important trade details, and close trades directly from the checklist.

Key Features:
- On-screen checklist: The checklist displays all open trades in a clear and organized manner, making it easy for traders to monitor their positions.
- Trade details: The checklist includes important trade details such as ticket number, symbol, trade type, lots, open price, close price, profit, and status.
- Close trades directly: Traders can close trades directly from the checklist by clicking the 'Close Trade' button. The robot will prompt for the close price and automatically calculate the profit.
- Automatic updates: The checklist display is automatically updated every minute to reflect the latest trade information.
- Customizable: Traders can customize the checklist display and adjust the layout according to their preferences.

Please note that ForexRobotEasy is not the official developer of Checklist MT4. We provide this sample code as an example of how the product can work. To find the official developer of Checklist MT4, please refer to MQL5.

For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/checklist-mt4-review-streamline-trading-with-on-screen-checklist/).
