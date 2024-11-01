# Stop-watch
#index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>STOP WATCH </title>
    <link rel="stylesheet" href="style.css">
    <script src="javascript.js" defer ></script>
</head>
<body>
    <div class="container">
        <h1>STOP WATCH</h1>
        <p><span id="second">00</span>:<span id="tens">00</span></p>
        <button id="btn-start">Start</button>
        <button id="btn-stop">Stop</button>
        <button id="btn-hold">Hold</button>
        <button id="btn-reset">Reset</button>
    </div>
</body>


</html>

#style.css

body{
    margin: 0%;
    padding: 0%;
    background: linear-gradient(to right,  rgb(144, 220, 144),  #0cc318,  #3cd61d);
}
.container{
    margin: 100px auto;
    text-align: center;
}
h1{
    font-size: 4em;
    font-family: Arial, Helvetica, sans-serif;
    color: #fff;
}
p{
    font-size: 5em;
    color: #fff;
}
button{
    border: none;
    padding: 18px 10px;
    font-size: 1.2em;
    width: 180px;
    margin: 10px;
}
button:hover{
    cursor: pointer;
    background-color: rgb(249, 249, 11);
    color: #fff;
    transition: 0.2s;
    border: none;
}
#javascript
var seconds = "00";
var tens = "00";
var OutputSeconds = document.getElementById('second');
var OutputTens = document.getElementById('tens');
var buttonStart = document.getElementById('btn-start');
var buttonStop = document.getElementById('btn-stop');
var buttonHold = document.getElementById('btn-hold');
var buttonReset = document.getElementById('btn-reset');
var Interval;

buttonStart.addEventListener('click', () => {
    clearInterval(Interval);
    Interval = setInterval(startTime, 10);
});
buttonStop.addEventListener('click', () => {
    clearInterval(Interval);
    
});
buttonHold.addEventListener('click', () => {
    clearInterval(Interval);
    tens = Stop;
    seconds = Stop;
    OutputSeconds.innerHTML = buttonStop;
    OutputTens.innerHTML = buttonStop;
});
buttonReset.addEventListener('click', () => {
    clearInterval(Interval);
    tens = "00";
    seconds = "00";
    OutputSeconds.innerHTML = seconds;
    OutputTens.innerHTML = tens;
});

function startTime(){
    tens++;
    if(tens <= 9){
        OutputTens.innerHTML = "0"+ tens;
    }
    if(tens > 9){
        OutputTens.innerHTML = tens;
    }
    if(tens > 99){
        seconds++;
        OutputSeconds.innerHTML = "0"+ seconds;
        tens = 0;
        OutputTens.innerHTML = "0"+tens;
    }
    if(seconds > 9){
        OutputSeconds.innerHTML = seconds;
    }
}


