<!DOCTYPE html>
<html>
    <body>
        <h2>Your Weather object from openweatermap.org.</h2>
        <div id="ipText"></div>
        <script>
            //var requestURL = "http://ip.jsontest.com";
            var requestURL = "http://api.openweathermap.org/data/2.5/weather?zip=97132,us&APPID=c3259b476fba8880191b6e087f87f2e9";
            var request = new XMLHttpRequest();
            request.open("GET", requestURL);
            request.responseType = "text";
            request.send();
            request.onreadystatechange = function () {
                var jsonObj = request.response;
                document.getElementById("ipText").innerHTML = jsonObj;
            }
        </script>

       <h2>My Longitude and Latitude from JSON object.</h2>
        <div id="ipJSONObject">
            <button type="button" onclick="getIP()">Weather Button</button>
        </div>
       <div id="ipJSONObject2"></div>
        <script>
            function getIP() {
                //var requestURL = "http://ip.jsontest.com";
                 var requestURL = "http://api.openweathermap.org/data/2.5/weather?zip=97132,us&APPID=c3259b476fba8880191b6e087f87f2e9";
                var request = new XMLHttpRequest();
                request.open("GET", requestURL);
                request.responseType = "json";
                request.send();
                request.onreadystatechange = function () {
                    var jsonObj = request.response;
                    document.getElementById("ipJSONObject").innerHTML = "Longitude: " + jsonObj.coord.lon;
                    document.getElementById("ipJSONObject2").innerHTML = "Latitude: " + jsonObj.coord.lat;
                }
            }
        </script>

        <br><a id="newaccount" href="https://johnson-robert.github.io/cit261/index.html">Click me and go Home!</a>
    </body>
</html>