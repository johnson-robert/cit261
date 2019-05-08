
<!DOCTYPE html>

<html>
    <head>
        <title>functions parameters</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
        <p id = "printMe1"></p>
        <p id = "printMe2"></p>
        <p id="demo"></p>
        <script>
            //function named myFunc
            var a;
            var b;
            var c;
            var x;
            
            function myFunc(a, b, c) {
                return a + b + c;
            }
            
            x = myFunc(2,3,4)
            document.getElementById("printMe1").innerHTML = x;
            
            //function stored as variable 
            var y = function(a, b, c) {
                return a * b * c
                };    
                document.getElementById("printMe2").innerHTML = y(2,3,4);
            
        </script>
    </body>
</html>
