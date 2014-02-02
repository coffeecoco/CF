////////////////////////////////////////////////////////////////////
//Programs
////////////////////////////////////////////////////////////////////
//A - Currency Arbitrage, Choose UtoU or BtoB arbitrage through L  - This should be fixed and tested 

//B - Portfolio Balancing, Maintain 50% of two currencies at all times - Alpha what is this?

//C - Custom trailing/advancing sell/sell bot for gna - Alpha what is this ?

//D - Buy Down, Buy 1/2 spread each .5 drop and sell 1 each $1 gain - microroll, is this a bug fix?

//E - Rolling sell/sell on dips and spikes V1,1.1,1.2,V2,2.1 - microroll, another todo list?

//F - 24 Hour high/low balancing bot, maintain (high-last)/(high-low) balance in USD and (last-low)/(high-low) in BTC - do we want this ?

//G - EMA triggered rolling with Fibonacci shares and high/low balancing combination with micro-trade re-balancing.
This appears to be on wish list, need this ? what other bits do we need to supply and test about this ?

//H - Custom Rolling bot based on dynamic thresholds, Is this apart of the micro roll engine?

//I - Micro-Trade rolling bot with variable buy and sell orders and iterations

//J - Revamped micro-rebalance engine added as option - balances based on distance to high low, microroll  bug fix?

////////////////////////////////////////////////////////////////////

todo list? lets amend these ?
//Advance and Tail last price with orders ( commision + profit/2 )
//Set order amounts to min < all < max
//Buy as price falls
//Sell as price rises
//USE triple EMA + last to determine trends
//USE distance from high/low to determine funds to sell/buy
//NOTE Buy at last - threshold ( amount is min ( maxtrade, rebalance percentage )
//NOTE num orders is set for buy and sell, use $incriment for order difference
//NOTE 100 orders sell would be price1+.01+.01 etc
//Don't sell unless last > EMA1 > EMA2 > EMA3
//Don't buy unless last < EMA1 < EMA2 < EMA3
//Use micro-orders to play on spikes and dips

Do we need to fix the stoploss
Is the stoploss starting back up properly
Is there a static or dynamic value to allow the bot to start up and re enter?
alpha i know you had feedback here
////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////
//USER CONFIGURABLE
////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////
//FEATURES
$DEBUG = FALSE; //Should the program Print Debug information
$simulate = FALSE; //RUNS IN SIMULATION MODE, NO TRADES ARE MADE just PRINT OUTPUT
$exchange = "E"; //Pick an exchange to run on
if ($exchange == "G") {$GOX = TRUE;$BTCE = FALSE;}
if ($exchange == "E") {$BTCE = TRUE;$GOX = FALSE;}

////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////
//ENGINE Selection
////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////
$ENGINE = "M";
//H - Hybrid Engine  - I have not tested this, hybird of what?
//E - EMA engine - Not tested this, but appears standard, but most likly broken
//S - Static Engine - what is this
//B - Filled Engine -  what is this
//FF - 50/50 Balance Engine  - what is this
//JOSH - JOSH's Trading Engine  - what is this
//JUDE - JUDE's Trading Engine - what is this
//M - Micro-roll engine 
//F This might be the FIB engine or something ?
