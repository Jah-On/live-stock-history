# live-stock-history
A home for archived live data. This is data that is often not saved afterwards like bid/ask. 

As of right now, this data only comes from TD Ameritrade. I will include data from other brokerages such as Ally or Fidelity if I reach $2500 in sponsors. 

Here is the hierarchy of this repository:

* live-stock-history
  * MIC (["Market Identifier Code"](https://www.iso20022.org/market-identifier-codes))
    * Symbol
      * year-month-day.txt

One line on the file will represent one minute (TD Ameritrade only allows 120 requests a minute : ( ). The file will __only__ include date from regular hours. I may consider adding a special tier to request pre/after data for one stock. 

For info on the data in each line, go [here](https://developer.tdameritrade.com/quotes/apis/get/marketdata/%7Bsymbol%7D/quotes).

Each text file is compressed with ZLIB. This helps with GitHub's storage limitations (and mine too!) and allows for larger data requests. 
