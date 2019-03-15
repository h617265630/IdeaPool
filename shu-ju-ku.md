\#  积分明细取数

SELECT TT.BLC\_OUT,   \#应收结算账套

T3.bebName AS OUT\_NAME, \#应收帐号名称

T1.TYPE\_NAME AS OUT\_TYPE\_NAME, \#积分类型

SUBSTRING\_INDEX\(T1.SALE\_SCODENAME,' ',-1\) AS SITOUT\_NAME, \# 网点名称

T1.SALE\_ORDERID, \#订单

ABS\(TT.PNT\_VAL\) AS PNT\_VAL, \#结算积分

FROM\_DAYS\(TT.REC\_TIME\_TDS\) AS OUT\_REC\_TIME, \#结算时间

TT.CHG\_FORMER, \#唯一键

SUBSTRING\_INDEX\(T2.SALE\_SCODENAME,' ',-1\) AS SITIN\_NAME,  \#应付网点

T2.TYPE\_NAME AS IN\_TYPE\_NAME,\#应付结算类型

IFNULL\(T2.SALE\_ORDERID,T2.MKT\_CODE\) SALE\_MKT\_ID,  \#应付订单号或活动

T2.MKT\_NAME, \#活动名称

FROM\_DAYS\(T2.REC\_TIME\_TDS\) AS IN\_REC\_TIME, \#应付时间

TT.BLC\_IN, \#应付id

T4.bebName AS IN\_NAME \#应付名称

FROM rpt\_tmp\_points\_out  TT 

LEFT JOIN rpt\_fac\_cst\_points\_change  T1 ON TT.CHG\_ID=T1.CHG\_ID

LEFT JOIN rpt\_fac\_cst\_points\_change  T2 ON TT.CHG\_FORMER=T2.CHG\_ID

LEFT JOIN mtbizsetofbook T3 ON TT.BLC\_OUT =T3.bebId

LEFT JOIN mtbizsetofbook T4 ON TT.BLC\_IN =T4.bebId

WHERE TT.BLC\_OUT='2' AND TT.BLC\_IN='1' AND TT.REC\_TIME\_TDS BETWEEN  TO\_DAYS\('2018-01-01'\) AND   TO\_DAYS\('2019-01-01'\);

