1. js 中页面展示不一样，页面不一样， js 中逻辑可能不一样



2. controller 里调用了 不一样的异步导出方法。



3. 





view   clear

js      pageOptions   有个exportCsv函数 调用url 

controller 

	CustomerPointSearchExport\(Request $request\)-&gt;asyncExportCSv\(\);

	

	也就是说basicController 里asyncExportCsv-&gt;ExportCsv\(\) 

	然后在handle里注册 

model

	然后再model里添加exportCsv方法

other





