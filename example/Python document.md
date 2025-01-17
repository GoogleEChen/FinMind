## Python
###### Arguments

* **dataset** : string.
* **stock_id** : list. USing for stock related dataset.
* **data_id** : list. USing for non stock related dataset, e.g exchange rate, crude oil prices.
* **date** : string. Data time interval is **date** ~ now.( e.g '2019-01-01' )

#### Example

* Load Taiwan Stock info 股票資訊

      from FinMind.Data import Load
      import requests
      import pandas as pd
      url = 'http://finmindapi.servebeer.com/api/data'
      list_url = 'http://finmindapi.servebeer.com/api/datalist'


      form_data = {'dataset':'TaiwanStockInfo',
                   'stock_id':'',
                   'date':''}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Taiwan Stock Price 股價

      form_data = {'dataset':'TaiwanStockPrice',
                   'stock_id':['2330','2317'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Taiwan Stock Financial Statements 財報

      form_data = {'dataset':'FinancialStatements',
                   'stock_id':['2330','2317'],
                   'date':'2019-01-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data = Load.transpose(data)
      data.head()

* Load Taiwan Stock Stock Dividend 股息股利

      form_data = {'dataset':'TaiwanStockStockDividend',
                   'stock_id':['2330','2317'],
                   'date':'2018-01-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()


* Load Taiwan Stock Margin Purchase Short Sale 融資融券

      form_data = {'dataset':'TaiwanStockMarginPurchaseShortSale',
                   'stock_id':['2330','2317'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Taiwan Stock Institutional Investors Buy Sell 個股外資買賣

      form_data = {'dataset':'InstitutionalInvestorsBuySell',
                   'stock_id':['2330','2317'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()


* Load Taiwan Stock Share holding 外資持股

      form_data = {'dataset':'Shareholding',
                   'stock_id':['2330','2317'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Taiwan Stock Balance Sheet 資產負債表

      form_data = {'dataset':'BalanceSheet',
                   'stock_id':['2330','2317'],
                   'date':'2019-01-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Taiwan Stock Holding Shares Per 股權分散表

      form_data = {'dataset':'TaiwanStockHoldingSharesPer',
                   'stock_id':['2330','2317'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Taiwan Stock Month Revenue 月營收

      form_data = {'dataset':'TaiwanStockMonthRevenue',
                   'stock_id':['2330','2317'],
                   'date':'2019-01-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load US Stock Info 美股股票資訊

      form_data = {'dataset':'USStockInfo',
                   'stock_id':'',
                   'date':''}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load US Stock Price 美股股價

      form_data = {'dataset':'USStockPrice',
                   'stock_id':['^GSPC','^DJI'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load US Stock Financial Statements 財報

      form_data = {'dataset':'FinancialStatements',
                   'stock_id':['AAPL'],
                   'date':'2018-01-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Japan Stock Info 日股股票資訊

      form_data = {'dataset':'JapanStockInfo',
                   'stock_id':'',
                   'date':''}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Japan Stock Price 日股股價

      form_data = {'dataset':'JapanStockPrice',
                   'stock_id':['1352.T','1376.T'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load UK Stock Info 英股股票資訊

      form_data = {'dataset':'UKStockInfo',
                   'stock_id':['2330','2317'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load UK Stock Price 英股股價

      form_data = {'dataset':'UKStockPrice',
                   'stock_id':['0TWH.L','0HZU.L'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load Europe Stock Info  歐股股票資訊

      form_data = {'dataset':'EuropeStockInfo',
                   'stock_id':'',
                   'date':''}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()


* Load Europe Stock Price 歐股股價

      form_data = {'dataset':'EuropeStockPrice',
                   'stock_id':['AB.PA','ABCA.PA'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load list of Exchange Rate 匯率列表


      form_data = {'dataset':'ExchangeRate',}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data


* Load Exchange Rate 匯率

      form_data = {'dataset':'ExchangeRate',
                   'data_id':['Canda', 'China', 'Euro', 'Japan', 'Taiwan', 'UK'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load list of Institutional Investors 外資列表


      form_data = {'dataset':'InstitutionalInvestors'}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data

* Load Institutional Investors 整體外資買賣


      form_data = {'dataset':'InstitutionalInvestors',
                   'data_id':['Dealer', 'Dealer_Hedging', 'Foreign_Investor', 'Investment_Trust'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()


* Load list of Interest Rate 各國利率列表

      form_data = {'dataset':'InterestRate'}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data


* Load Interest Rate 利率

      form_data = {'dataset':'InterestRate',
                   'data_id':['BCB','BOC',],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()


* Load list of Government Bonds 政府債券列表

      form_data = {'dataset':'GovernmentBonds'}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data

* Load Government Bonds 政府債券


      form_data = {'dataset':'GovernmentBonds',
                   'data_id':['France 9-Month','France 9-Year'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load list of Crude Oil Prices 油價列表

      form_data = {'dataset':'CrudeOilPrices'}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data

* Load Crude Oil Prices 油價

      form_data = {'dataset':'CrudeOilPrices',
                   'data_id':['Brent', 'WTI'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load list of Raw Material Futures Prices 原物料期貨列表

      form_data = {'dataset':'RawMaterialFuturesPrices'}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data

* Load Raw Material Futures Prices 原物料期貨

      form_data = {'dataset':'RawMaterialFuturesPrices',
                   'data_id':['US Corn Futures','US Soybean Meal Futures',],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()


* Load Gold Price 金價

      form_data = {'dataset':'GoldPrice','date':'2019-06-06'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()

* Load list of Currency Circulation 

      form_data = {'dataset':'CurrencyCirculation'}
      res = requests.post(
              list_url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = temp['data']
      data

* Load Currency Circulation


      form_data = {'dataset':'CurrencyCirculation',
                   'data_id':['Europe', 'Taiwan','US'],
                   'date':'2019-06-01'}
      res = requests.post(
              url,verify = True,headers = {},
              data = form_data)

      temp = res.json()
      data = pd.DataFrame(temp['data'])
      data.head()
