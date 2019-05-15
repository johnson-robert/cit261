<!DOCTYPE html>

<html>
    <head>
        <title>functions parameters</title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <body>
        
        <p id="printMe1"></p>
        <p id="printMe2"></p>
        <p id="printMe3"></p>
        <p id="printMe4"></p>
        <script>
            //array
            var motorcycles = ["Ducati", "Honda", "Triumph"];
            motorcycles[3] = "Moto Guzzi";
            document.getElementById("printMe1").innerHTML = motorcycles[0] + ", " + motorcycles[1] + ", " + motorcycles[2] + ", " + motorcycles[3];   
  
            //array of arrays
            var ducati = ["Monster", "1999"];
            var honda = ["Nx250", "1989"];
            var motoGuzzi = ["Breva", "2008"];
            var triumph = ["Thunderbird", "1999"];
            var moto = [ducati, honda, motoGuzzi, triumph];
            var i;
            
            for (i = 0; i < moto.length; i++) {
                document.getElementById("printMe2").innerHTML = moto;
            }
            
            //array of object pairs
            var ducati = {model : "Monster", year : "1999"};
            var honda = {model : "Nx250", year : "1989"};
            var motoGuzzi = {model : "Breva", year : "2008"};
            var triumph = {model : "Thunderbird", year : "1998"};
            var motos = [ducati, honda, motoGuzzi, triumph];
            var i;
            var text = "Motorcycles:";
            
            for (i = 0; i < motos.length; i++) {
                text += "</br>" + motos[i].model + ", " +  motos[i].year;
            }
            document.getElementById("printMe3").innerHTML = text;
            
        </script>    
    </body>
</html>


