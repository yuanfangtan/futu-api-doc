.. role:: strike
    :class: strike
.. role:: red-strengthen
    :class: red-strengthen

.. _FutuOpenD: ../intro/FutuOpenDGuide.html

介绍
====================
py-futu-api依赖FutuOpenD网关客户端，需要先运行登录 FutuOpenD_



交易品种:
::

          1.港股：正股、ETF、窝轮、牛熊证
          2.美股：正股、ETF
行情数据:
::
          1.支持A股、港股
          2.支持定阅并接收实时报价、逐笔、买卖档，买卖经纪（仅港股)等深度数据

--------------

  .. _get_trading_days: Quote_API.html#get_trading_days
  .. _get_stock_basicinfo: Quote_API.html#get_stock_basicinfo
  .. _get_multiple_history_kline: Quote_API.html#get_multiple_history_kline
  .. _get_autype_list:  Quote_API.html#get_autype_list
  .. _get_market_snapshot:  Quote_API.html#get_market_snapshot
  .. _get_rt_data:  Quote_API.html#get_rt_data
  .. _get_plate_stock:  Quote_API.html#get_plate_stock
  .. _get_plate_list:  Quote_API.html#get_plate_list
  .. _get_broker_queue:  Quote_API.html#get_broker_queue
  .. _subscribe:  Quote_API.html#subscribe
  .. _get_stock_quote:  Quote_API.html#get_stock_quote
  .. _get_rt_ticker:  Quote_API.html#get_rt_ticker
  .. _get_cur_kline:  Quote_API.html#get_cur_kline
  .. _get_order_book:  Quote_API.html#get_order_book
  .. _get_multi_points_history_kline:  Quote_API.html#get_multi_points_history_kline
  .. _get_referencestock_list:  Quote_API.html#get_referencestock_list
  .. _get_owner_plate:  Quote_API.html#get_owner_plate
  .. _get_holding_change_list:  Quote_API.html#get_holding_change_list
  .. _request_history_kline: Quote_API.html#request_history_kline
  .. _query_subscription: Quote_API.html#query_subscription
  .. _get_warrant: Quote_API.html#get_warrant
  .. _get_option_chain:  Quote_API.html#get_option_chain
  .. _get_history_kl_quota: Quote_API.html#get_history_kl_quota
  .. _get_rehab: Quote_API.html#get_rehab
  .. _unsubscribe_all: Quote_API.html#unsubscribe_all
  .. _get_capital_flow: Quote_API.html#get_capital_flow
  .. _get_capital_distribution: Quote_API.html#get_capital_distribution
  .. _get_user_security: Quote_API.html#get_user_security
  .. _modify_user_security: Quote_API.html#modify_user_security
  .. _get_stock_filter: Quote_API.html#get_stock_filter  
  .. _get_future_info: Quote_API.html#get_future_info
  .. _request_trading_days: Quote_API.html#request_trading_days
  .. _set_price_reminder: Quote_API.html#set_price_reminder
  .. _get_price_reminder: Quote_API.html#get_price_reminder
  .. _get_ipo_list: Quote_API.html#get_ipo_list

  .. _get_acc_list:  Trade_API.html#get_acc_list
  .. _unlock_trade:  Trade_API.html#unlock_trade
  .. _accinfo_query:  Trade_API.html#accinfo_query
  .. _position_list_query:  Trade_API.html#position_list_query
  .. _place_order:  Trade_API.html#place_order
  .. _order_list_query:  Trade_API.html#order_list_query
  .. _modify_order:  Trade_API.html#modify_order
  .. _deal_list_query: Trade_API.html#deal_list_query
  .. _history_order_list_query: Trade_API.html#history_order_list_query
  .. _history_deal_list_query: Trade_API.html#history_deal_list_query
  .. _acctradinginfo_query: Trade_API.html#acctradinginfo_query
  

---------------------------------------------------
 
主要函数列表
----------

行情函数:

================================    ============================================================================
函数名                                 功能简介
================================    ============================================================================
get_stock_basicinfo_                获取指定市场中特定类型的股票基本信息
request_history_kline_              获取k线，不需要事先下载k线数据
get_history_kl_quota_               获取已使用过的额度，即当前周期内已经下载过多少只股票
get_rehab_                          获取给定股票的复权因子
get_market_snapshot_                获取市场快照
get_rt_data_                        获取指定股票的分时数据
get_plate_stock_                    获取特定板块下的股票列表
get_plate_list_                     获取板块集合下的子板块列表
get_broker_queue_                   获取股票的经纪队列
subscribe_                          订阅注册需要的实时信息，指定股票和订阅的数据类型即可，港股订阅需要Lv2行情。
unsubscribe_all_                    取消该实例的所有订阅
query_subscription_				    查询订阅信息
get_stock_quote_                    获取订阅股票报价的实时数据，有订阅要求限制
get_rt_ticker_                      获取指定股票的实时逐笔。取最近num个逐笔
get_cur_kline_                      实时获取指定股票最近num个K线数据
get_order_book_                     获取实时摆盘数据
get_referencestock_list_            获取证券的关联数据
get_owner_plate_                    获取单支或多支股票的所属板块信息列表
get_holding_change_list_            获取大股东持股变动列表,只提供美股数据,并最多只返回前100个
get_option_chain_                   通过标的股查询期权
get_warrant_                        拉取窝轮和相关衍生品数据接口
get_capital_flow_                   获取个股资金流向
get_capital_distribution_           获取个股资金分布
get_user_security_                  获取指定分组的自选股列表
modify_user_security_               修改指定分组的自选股列表
get_stock_filter_                   获取条件选股
get_ipo_list_                       获取指定市场的ipo列表
get_future_info_                    获取期货合约资料
request_trading_days_               在线请求交易日
set_price_reminder_                 设置到价提醒
get_price_reminder_                 获取对某只股票(某个市场)设置的到价提醒列表
================================    ============================================================================

交易函数:

================================    ============================================================================
函数名                                 功能简介
================================    ============================================================================
get_acc_list_                       获取交易业务账户列表
unlock_trade_                       解锁交易
accinfo_query_                      获取账户资金数据
position_list_query_                获取账户持仓列表
place_order_                        下单
order_list_query_                   获取订单列表
modify_order_                       修改订单
deal_list_query_                    获取成交列表
history_order_list_query_           获取历史订单列表
history_deal_list_query_            获取历史成交列表
acctradinginfo_query_               查询账户下最大可买卖数量
================================    ============================================================================






	
	
	

