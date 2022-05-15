## add this script to your script
call checkCookie() when you want block device                                                                                                                              

132 of the 365 chalenge in 2022 1 day 1 challenge

```javascript      
      function setCookie(cname,cvalue,exdays) {
            const d = new Date();
            d.setTime(d.getTime() + (exdays*24*60*60*1000));
            let expires = "expires=" + d.toUTCString();
            document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
        }

        function getCookie(cname) {
            let name = cname + "=";
            let decodedCookie = decodeURIComponent(document.cookie);
            let ca = decodedCookie.split(';');
            for(let i = 0; i < ca.length; i++) {
                let c = ca[i];
                while (c.charAt(0) == ' ') {
                    c = c.substring(1);
                }
                if (c.indexOf(name) == 0) {
                    return c.substring(name.length, c.length);
                }
            }
            return "";
        }

        function checkCookie() {
            let user = getCookie("username");
            var loc=window.location.href;
            var num = 0;
            var index = loc.indexOf("?");
            index += 1;
            var x = loc.substring(index);

            if (user != "") {
                location.replace("https://liad07.github.io/banme/banme?"+x.toString()) ;
        document.getElementById("site").textContent=window.location.href;
            } else {
                user = window.location.href;
                if (user != "" && user != null) {
                    setCookie("username", user, 30);
                }
            }
        }

