# live-stock-history
A home for archived live data. This is data that is often not saved afterwards like bid/ask. 

As of right now, this data only comes from TD Ameritrade. With this, I can only get data for U.S. stocks. If I reach for evey $1,000 in sponsors, another country will be added. 

Here is the hierarchy of this repository:

* live-stock-history
  * MIC (["Market Identifier Code"](https://www.iso20022.org/market-identifier-codes))
    * Symbol
      * year-month-day.txt

One line on the file will represent ten seconds. The file will __only__ include date from regular hours. I may consider adding a special tier to request pre/after data for one stock. 

For info on the data in each line, go [here](https://developer.tdameritrade.com/quotes/apis/get/marketdata/%7Bsymbol%7D/quotes).

Each text file is compressed with ZLIB. This helps with GitHub's storage limitations (and mine too!) and allows for larger data requests. 
