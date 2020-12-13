# IB-Data-Download
From wrighter/download_bars.py (https://gist.github.com/wrighter/dd201adb09518b3c1d862255238d2534, Article: https://dev.to/wrighter/how-to-get-historical-market-data-from-interactive-brokers-using-python-3bcn)

Some improvements:

- Added existing files detected, for resuming broken downloads.
- Changed data path, especially for Forex data
- Add API host and port args

Setup:
1, Place IB API Python package into /ibapi
2, Run TWS or Gateway
3, Run as command (just change the arguments as you are using):

   python download_bars.py --size "1 min" --security-type CASH --exchange IDEALPRO --start-date 20130101 --end-date 20201204 --host 127.0.0.1 --port 4002 --currency USD EUR -t ASK

4, If sometimes downlowd is broken, then run the command again, and it will resume from where you have downloaded.




