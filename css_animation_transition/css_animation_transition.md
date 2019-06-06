<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://johnson-robert.github.io/cit261/images/favicon.ico" type="image/x-icon" rel="shortcut icon">
        <link href="https://johnson-robert.github.io/cit261/css/main.css" rel="stylesheet">
        <!--<link href="../css/main.css" rel="stylesheet">-->
        <title>CIT 261 Assignment Portal | Rob Johnson | BYU-Idaho</title>
    </head>
    <body>


        <p><button class="buttonOne" onclick="changeColor()">Change My Color</button></p> 
        <p><button class="buttonTwo" onclick="flipIt()">Flip</button></p>
        <p><button class="buttonThree" onclick="flopIt()">Flop</button></p>
        <p><button class="buttonFour" onclick="moveHelo()">Fly</button></p>

        <div class="motorBox">
            <img class="helo" src="https://johnson-robert.github.io/cit261/images/helicopter.PNG"  height="75" alt="Helicopter"/>
        </div>
        <div class="motorBox">
            <img id="motorCycle" class="motor" src="https://johnson-robert.github.io/cit261/images/motorcycle.PNG"  alt="Helicopter"/>
        </div>
        <p><button class="buttonFive" onclick="goMoto()">Ride</button></p>
        <script>
            function changeColor() {
                document.getElementsByTagName("button")[0].setAttribute("id", "color");
            }
            function flipIt() {
                document.getElementsByClassName("buttonTwo")[0].setAttribute("id", "flip");
                document.getElementsByClassName("helo")[0].setAttribute("id", "flip");
            }
            function flopIt() {
                document.getElementsByClassName("buttonTwo")[0].removeAttribute("id");
                document.getElementsByClassName("helo")[0].removeAttribute("id");
            }
            function moveHelo() {
                document.getElementsByClassName("buttonFour")[0].setAttribute("id", "color");
                document.getElementsByTagName("img")[0].setAttribute("id", "fly");
            }
            function goMoto() {
                var x = 0;
                setInterval(go,5);
                function go() {
                    if (x < 350) {
                        x++;
                        document.getElementById("motorCycle").style.left = x + 'px';
                    }
                    else {
                        document.getElementsByClassName("motor")[0].setAttribute("id", "flip");
                    }
                }
            }

        </script>



    </body>
</html>

