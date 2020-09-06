# cloudflare-proxyweb
#  
# 添加workers  
  代码：  
    addEventListener(  
  "fetch",event => {  
    let url=new URL(event.request.url);  
    url.hostname="网址，不带http前缀";  
    let request=new Request(url,event.request);  
    event. respondWith(  
      fetch(request)  
    )  
  }  
)  
