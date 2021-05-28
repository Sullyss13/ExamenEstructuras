# ExamenEstructuras
<!DOCTYPE html>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
    <link href="Content/bootstrap.css" rel="stylesheet"/>
<link href="Content/site.css" rel="stylesheet"/>

    <script src="Scripts/modernizr-2.8.3.js"></script>

</head>
<body>
    <div class="navbar navbar-inverse navbar-fixed-top">
        <div class="container">
            <div class="navbar-header">
                <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                    <span class="icon-bar"></span>
                </button>
                <a class="navbar-brand" href="/">Examen</a>
            </div>
            <div class="navbar-collapse collapse">
              
            </div>
        </div>
    </div>
    <div class="container body-content">
        


<div class="jumbotron">
  revision de validacion
</div>

<div class="row">
   
  <input type="text" id="palabra" />

</div>
<input type="button" onclick="myfunction();" value="Revisar" />

<label id="texto"></label>

<script>

    
    function myfunction() {
        //DECLARAMOS MIS VARIABLES
        var palabra = $("#palabra").val();
       
        var original = palabra;
        var array = palabra.split("");
        
        var reversa = "";
        for (var i = 0; i < array.length; i++) {

            var pos = i + 1;
            console.log(array[i] + ' ' + pos +' '+ makeid(pos,array[i]));
        }

      
    }


    function makeid(length,inicial) {
    var result           = [];
    var characters       = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz';
        var charactersLength = characters.length;

    for ( var i = 0; i < length; i++ ) {
      result.push(characters.charAt(Math.floor(Math.random() * 
       charactersLength)));
    }

        if (inicial == " ") {
            return "";
        }
        var salida = "";
        for (var i = 0; i < length; i++) {

            
             var newString = result.join('');
        newString = inicial + newString.substring(1);
            salida += newString+',';
        }
        return salida;
    }




</script>
        <hr />
        <footer>
            <p>&copy; 2021 - Mi aplicación ASP.NET</p>
        </footer>
    </div>

    <script src="Scripts/jquery-3.3.1.js"></script>

    <script src="Scripts/bootstrap.js"></script>

    
</body>
</html>
