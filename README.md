# DAX
Prior Sales = 
   calculate( [Total_SALES],
      parallelperiod( Dates[Order_Date], -1, YEAR) )

Cumulative Sales = 
VAR CumulativeTotal = CALCULATE( [Total_SALES],
                        FILTER( ALLSELECTED( Dates[Order_Date] <= MAX( Dates[Order_Date]) ) )

% Sales vs LY = DIVIDE( [Cumulative Sales], [Prior Sales], 0 )
