# The SIAM.mq5 ReadMe File

## Overview

The SIAM.mq5 is a trading robot developed by Forex Robot Easy Team. It is designed to trade on the Forex market using a virtual channel indicator and Average True Range (ATR) indicator for decision making.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/the-siam-review-profitable-gold-trading-software-solution/). Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. To find the official developer of this product, please refer to MQL5.

## Features

- The SIAM.mq5 uses a virtual channel indicator to identify potential buying and selling opportunities.
- The robot incorporates the Average True Range (ATR) indicator to determine the volatility of the market.
- It has a fixed stop loss value to limit potential losses.
- The Recovery Factor parameter allows for profit tracking and recovery in case of adverse market conditions.

## Input Parameters

- StopLoss: This parameter sets the fixed stop loss value for each trade.
- VirtualChannelPeriod: It determines the period for the virtual channel indicator.
- ATRPeriod: This parameter specifies the period for the Average True Range (ATR) indicator.
- RecoveryFactor: It sets the recovery factor for profit tracking and recovery model.

## Global Variables

- ticket: This variable stores the trade ticket number.
- virtualChannelUpper: It holds the value of the upper level of the virtual channel indicator.
- virtualChannelLower: This variable stores the value of the lower level of the virtual channel indicator.

## Initialization Function

The OnInit() function is called when the robot is initialized. In this function, the virtual channel levels are calculated based on the previous candle's high and low values, along with the ATR indicator values.

## Trading Function

The OnTick() function is called on every tick of the market. In this function, the robot checks if there is an open trade and if trading is allowed. If so, it checks if the price is above the virtual channel upper level or below the virtual channel lower level. Based on these conditions, the robot opens a buy or sell trade using the OrderSend() function.

## Trade Allowance Function

The IsTradeAllowed() function is used to check if trading is allowed. It first checks if there is an open trade stored in the ticket variable. If there is no open trade, it allows new trades. If there is an open trade, it checks if the trade is still open or closed. If the trade is closed, it allows new trades. If the trade is still open, it does not allow new trades.

Please note that this code is provided as a sample and may require modifications or additional functionalities to suit individual trading strategies.
