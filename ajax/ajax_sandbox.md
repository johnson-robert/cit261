<!DOCTYPE html>
<html>
    <body>
        <h2>Weather as text from JSON file.</h2>
        <div id="weatherButton">
            <button type="button" onclick="dataSet()">Weather Button</button>
        </div>

        <script>
            function dataSet() {
                var xhttp = new XMLHttpRequest();
                xhttp.onreadystatechange = function () {
                    if (this.readyState == 4 && this.status == 200) {
                        document.getElementById("weatherButton").innerHTML =
                                this.responseText;
                    }
                    if (this.readyState == 4 && this.status == 401) {
                        document.getElementById("weatherButton").innerHTML =
                                this.responseText;
                    }
                };

                xhttp.open("GET", "http://api.openweathermap.org/data/2.5/weather?zip=97132,us&APPID=c3259b476fba8880191b6e087f87f2e9", true);
                xhttp.send();
            }
        </script>

        <br><a id="newaccount" href="https://johnson-robert.github.io/cit261/index.html">Click me and go Home!</a>
    </body>
</html>
