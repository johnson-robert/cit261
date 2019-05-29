<!DOCTYPE html>

<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://johnson-robert.github.io/cit261/images/favicon.ico" type="image/x-icon" rel="shortcut icon">
        <link href="https://johnson-robert.github.io/cit261/css/main.css" rel="stylesheet">
        <title>CIT 261 Assignment Portal | Rob Johnson | BYU-Idaho</title>
    </head>
    <body>
        <h3>So Many Ways To Save Time</h3>
        <h4>Storing objects in .localStorage</h4>




        <p>Current Time: <span id="printMe1"></span></p>
        <button onclick="CheckForBrowserSupport()">Check to see if browser supports .localStorage</button><br>
        <p><span id="printMe2"></span></p>
        <button onclick="SaveToLocalStorage()">Save date to .localStorage</button><br>
        <p>The time saved is: <span id="printMe3"></span></p>
        <button onclick="RemoveFromLocalStorage()">Remove from .localStorage</button><br><br><br>
        <button onclick="SaveToLocalStorage2()">Save date to .localStorage in JSON format</button><br>
        <p><span id="printMe4"></span></p>
        <button onclick="RetrieveFromLocalStorage2()">Retrieve date from .localStorage</button>
        <p><span id="printMe5"></span></p><br>
        <p><button onclick="clickCounter()" type="button">Click me many times!</button></p>
        <p><span id="printMe6"></span></p>
        <input type="button" value="Clear .sessionStorage" onClick="ClearSessionCounter()"><br>

        <script>
            //check for browser support
            function CheckForBrowserSupport() {
                if (typeof (Storage) !== "undefined") {
                    document.getElementById("printMe2").innerHTML = "Your browser has .localStorage support.";
                } else {
                    document.getElementById("printMe2").innerHTML = "Ohh..no. Your browser doesn't have .localStorage support.";
                }
            }
            //get the time and date
            var tim = new Date().getTime();
            var dat = new Date();
            var today = dat.getMonth() + "/" + dat.getDay() + "/" + dat.getFullYear();
            document.getElementById("printMe1").innerHTML = tim;

            //save time to localStorage
            //localStorage has no expiration date
            function SaveToLocalStorage() {
                localStorage.curtim = tim;

                //print curtime from localStorate
                document.getElementById("printMe3").innerHTML = localStorage.curtim;
            }
            //remove curtime from localStorage
            function RemoveFromLocalStorage() {
                localStorage.removeItem("curtim");

                //print curtim show undefined 

                document.getElementById("printMe3").innerHTML = localStorage.curtim;
            }

            //removes previously stored value
            localStorage.clear();
            //saves name:value jpair to localStorage
            function SaveToLocalStorage2() {
                var datJSON = JSON.stringify(today)
                localStorage.setItem("storedDate", datJSON);
                document.getElementById("printMe4").innerHTML = datJSON;
            }
            //retrieves data from .localStorage
            var datRetrieved;
            function RetrieveFromLocalStorage2() {
                var text = localStorage.getItem("storedDate");
                datRetrieved = JSON.parse(text);
                document.getElementById("printMe5").innerHTML = datRetrieved;
            }

            function clickCounter() {
                    if (sessionStorage.clickcount) {
                        sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
                    } else {
                        sessionStorage.clickcount = 1;
                    }
                    document.getElementById("printMe6").innerHTML = "You have clicked the button " + sessionStorage.clickcount + " time(s) in this session.";
            }
            function ClearSessionCounter() {
                sessionStorage.clear();
                document.getElementById("printMe6").innerHTML = "";
            }

        </script>
        <br><a id="newaccount" href="https://johnson-robert.github.io/cit261/index.html">Click me and go Home!</a>
    </body>
</html>

