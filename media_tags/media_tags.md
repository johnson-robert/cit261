<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://johnson-robert.github.io/cit261/images/favicon.ico" type="image/x-icon" rel="shortcut icon">
        <link href="css_transition.css" rel="stylesheet">
        <title>CIT 261 Assignment Portal | Rob Johnson | BYU-Idaho</title>
    </head>
    <body>
        <p class="outsideBox">
            <span class="insideBox">Mouse over the Emoji.</span>
        <p>           
        <p class="labeler">transform: rotate3d()</p> 
        <div class="divOne">
            <img src="../images/smile_emoji_200_200.jpg" alt="Smile Emoji"/>
        </div>
        <p class="labeler">transform: translateX()</p>
        <div class="divTwo">
            <img src="../images/half_smile_emoji_200_200.jpg" alt="Half Smile Emoji"/>
        </div>
        <p class="labeler">transform: rotate(): transform can be animated.</p>
        <div class="divThree">
            <img src="../images/emoji_wink_236_236.jpg" alt="Emoji In Black Box"/>
        </div>
        <input class="buttonOne" type="button" value="Click me to make the Emoji round again." onClick="funcFour()">

        <script>
            document.getElementsByTagName("div")[0].addEventListener("mouseover", funcOne);
            document.getElementsByTagName("div")[1].addEventListener("mouseover", funcTwo);
            document.getElementsByTagName("div")[2].addEventListener("mouseover", funcThree);

            function funcOne() {
                document.getElementsByTagName("img")[0].setAttribute("class", "oneOne");
                var x = document.getElementsByTagName("img")[0].id;
                if (x === "" || x === "oneOne") {
                    document.getElementsByTagName("img")[0].setAttribute("id", "oneTwo");
                } else if (x === "oneTwo") {
                    document.getElementsByTagName("img")[0].setAttribute("id", "oneThree");
                } else {
                    document.getElementsByTagName("img")[0].setAttribute("id", "oneOne");
                }
            }
            function funcTwo() {
                var x = document.getElementsByTagName("img")[1].id;
                if (x === "" || x === "twoOne") {
                    document.getElementsByTagName("img")[1].setAttribute("id", "twoTwo");
                } else if (x === "twoTwo") {
                    document.getElementsByTagName("img")[1].setAttribute("id", "twoThree");
                } else {
                    document.getElementsByTagName("img")[1].setAttribute("id", "twoOne");
                }
            }
            function funcThree() {
                document.getElementsByTagName("img")[2].setAttribute("id", "threeOne");
            }
            function funcFour() {
                document.getElementsByTagName("img")[2].setAttribute("class", "fourOne");
            }
        </script>
        <br><a id="newaccount" href="https://johnson-robert.github.io/cit261/index.html">Click me and go Home!</a>
    </body>
</html>



