Если вы разрабатываете сайт локально и хотите протестировать его на боевом ресте,
вы не сможете отправлять запросы через AJAX из-за CORS. 
Вам поможет [дополнение](https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi), 
которое позволит отключить для выбранных доменов. 

Не забудьте сразу прописать в настрйоках более конкретный фильтр url. 
Например, `*://*.my.site/*` чтобы CORS был отключен толкьо на домене `my.site`
