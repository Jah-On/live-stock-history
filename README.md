# live-stock-history
A home for archived live data. This is data that is often not saved afterwards like bid/ask. 

As of right now, this data only comes from TD Ameritrade. With this, I can only get data for U.S. stocks. For evey $750 in sponsors, another country will be added (Not aall listings, just support for that country). 

Here is the hierarchy of this repository:

* live-stock-history
  * MIC (["Market Identifier Code"](https://www.iso20022.org/market-identifier-codes))
    * Symbol
      * year-month-day.txt

One line on the file will represent three seconds, with some exceptions. There may be times where TD Ameritrade does not send the right data back for a symbol, in which case the code will copy the last known data. In the extremely rare event that there is no last known poin, it will skip over that time and move on. The file will __only__ include date from regular hours. I will add after hours one I reach $1,000 in sponsors. 

For info on the data in each line, go [here](https://developer.tdameritrade.com/quotes/apis/get/marketdata/%7Bsymbol%7D/quotes).

Each text file is compressed with ZLIB. This helps with GitHub's storage limitations (and mine too!) and allows for larger data requests. 
