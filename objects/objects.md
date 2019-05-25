<!DOCTYPE html>

<html>
    <head>
        <title>functions parameters</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
        <b>Javascript objects can contain 1 or more values.</b>
        <p id="printMe1"></p>
        <b>Objects containing multiple values.</b>
        <b>They also can contain other objects.</b>
        <p id="printMe2"></p>
        <b>Object literal cantains name:value pairs.</b>
        <b>The name of the value, like model and year, are properties of the object.</b>
        <p id="printMe3"></p>
        <b>Using built in method to get values of the object.</b>
        <p id="printMe4"></p>
        <p id="printMe5"></p>
        <b>Objects can contain functions and methods.</b>
        <p id="printMe6"></p>
        <b>OR</b>
        <p id="printMe7"></p>
        <b>Instantiation - Object constructor</b>
        <p id="printMe8"></p>
        <script>
            //Javascript objects can contain 1 or more values 
            var motorcycles = ["Ducati", "Honda", "Triumph"];
            motorcycles[3] = "Moto Guzzi";
            //accessing the values of the object motorcycles
            document.getElementById("printMe1").innerHTML = motorcycles[0] + ", " + motorcycles[1] + ", " + motorcycles[2] + ", " + motorcycles[3];

            //objects can be single variables
            var model = "ducati";

            //objects containing multiple values
            var ducati = [model, "1999"];
            var honda = ["Nx250", "1989"];
            var motoGuzzi = ["Breva", "2008"];
            var triumph = ["Thunderbird", "1999"];

            //object of objects
            var moto = [ducati, honda, motoGuzzi, triumph];

            for (var i = 0; i < moto.length; i++) {
                document.getElementById("printMe2").innerHTML = moto;
            }

            //object literal cantains name:value pairs
            //the name of the value, like model and year, are properties of the object
            var ducati = {model: "Monster", year: "1999"};
            var honda = {model: "Nx250", year: "1989"};
            var motoGuzzi = {model: "Breva", year: "2008"};
            var triumph = {model: "Thunderbird", year: "1998"};

            var motos = [ducati, honda, motoGuzzi, triumph];

            var text = "Motorcycles:";

            for (var i = 0; i < motos.length; i++) {
                text += "</br>" + motos[i].model + ", " + motos[i].year;
            }
            document.getElementById("printMe3").innerHTML = text;

            //using a built in method to get properties of object
            var keys = Object.keys(ducati);
            document.getElementById("printMe4").innerHTML = keys;

            //using built in method to get values of the object
            var values = Object.values(ducati);
            document.getElementById("printMe5").innerHTML = values;
            
            //objects can contain functions
            motos.yourBike = function() {return "Your " + model.toString() +  
                        " is a " + ducati.year + " " + ducati.model + "."};
            document.getElementById("printMe6").innerHTML = motos.yourBike();
            
            //OR
            text = "";
            motos.yourBikes = function() {for (var i = 0; i < motos.length; i++) {
                text += "</br>" + motos[i].model + ", " + motos[i].year;
            }return text};
            document.getElementById("printMe7").innerHTML = motos.yourBikes();
            
            //Instantiation - Object constructor
            function addBike(yr, mk, md){
                this.yr = yr;
                this.mk = mk;
                this.md = md;
            };
            
            //create new object. 
            var garage =  new addBike("1978", "Suzuki", "TC100");
            document.getElementById("printMe8").innerHTML = garage.yr + " " + garage.mk + " " + garage.md;    
            
            
        </script>
        <br><a id="newaccount" href="https://johnson-robert.github.io/cit261/index.html">Click me and go Home!</a>
    </body>
</html>




