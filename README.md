# Mini Modify SL & TP Fixed MT5

This code is a sample implementation of a MetaTrader 5 (MT5) Expert Advisor (EA) called 'Mini Modify SL & TP Fixed MT5'. It is designed to modify the stop loss (SL) and take profit (TP) levels of an existing open position or a new order in real-time.

## Input Parameters

- `StopLoss`: Initial stop loss value (default: 50 pips)
- `TakeProfit`: Initial take profit value (default: 100 pips)

## Global Variables

- `ticket`: Order ticket number
- `modifyInProgress`: Flag to indicate if modification is in progress

## How It Works

The EA operates in the `OnTick()` function, which is called on every tick of the price. Here's a step-by-step breakdown of the code:

1. Check if modification is already in progress (`modifyInProgress` flag).
2. If modification is in progress, monitor the order modification progress.
   - Select the order based on its ticket number.
   - Check if the modification is completed by comparing the current SL and TP values with the desired values (`StopLoss` and `TakeProfit`).
   - If the modification is not completed, modify the order with the desired SL and TP values.
   - If the modification fails, print an error message and set `modifyInProgress` flag to false.
   - Return to the main execution loop.
3. If modification is not in progress, check if there is an open position.
   - Select the open position.
   - Get the ticket number of the open position.
   - Modify the order with the desired SL and TP values.
   - If the modification fails, print an error message.
   - Set `modifyInProgress` flag to true.
   - Return to the main execution loop.
4. If there is no open position, open a new order.
   - Send an order to buy with a volume of 0.01 lots at the current Ask price.
   - Store the order ticket number.
   - If the order fails to open, print an error message.
   - Set `modifyInProgress` flag to true.
   - Return to the main execution loop.

Please note that this code is provided as a sample and is not the official product developed by Forex Robot Easy Team. To find the official developer of this product, please refer to MQL5.

## Product Description

[Mini Modify SL & TP Fixed MT5](https://forexroboteasy.com/forex-robot-review/mini-modify-sl-tp-fixed-mt5-review-quick-automated-forex-tool/) is a powerful and flexible MetaTrader 5 Expert Advisor that allows you to easily modify the stop loss and take profit levels of your open positions or new orders. With its real-time modification capability, you can react quickly to changing market conditions and optimize your trading strategy.

Key Features:
- Dynamic SL and TP modification for existing open positions or new orders.
- Customizable initial SL and TP values.
- Real-time monitoring of order modification progress.
- Error handling and reporting for failed order modifications.
- Automatic execution on every tick of the price.

By using Mini Modify SL & TP Fixed MT5, you can enhance your trading experience and take control of your risk management. It is a valuable tool for both beginner and experienced traders who want to maximize their profitability and minimize their losses.

Please note that Forex Robot Easy Team is not the official developer of this product. We provide this sample code as an illustration of how the product can work based on its description. For detailed reviews and trading results of the official product, please refer to the provided backlink: [Mini Modify SL & TP Fixed MT5 Review](https://forexroboteasy.com/forex-robot-review/mini-modify-sl-tp-fixed-mt5-review-quick-automated-forex-tool/)
