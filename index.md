---
layout: detect
---

<!-- 브라우저 언어체크  -->
<script type="text/javascript">
    var userLang = navigator.language || navigator.userLanguage; 
    // var res = userLang.split("-"); 
    // window.location.href += res[1].toLowerCase();
    
    $.getJSON("http://ipinfo.io",function(data){
        ip = data.ip;
        hostname = data.hostname;
        city = data.city;
        country = data.country;
        loc = data.loc;
        org = data.org;

        window.location.href += country.toLowerCase();
    });

</script>