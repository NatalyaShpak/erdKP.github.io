<!doctype html>
<html>
<head>
<meta charset="UTF-8">
<script src="http://code.jquery.com/jquery-1.9.1.js"></script>
<title>Kompv2-Ui-entities</title>
<style>
body {
    font-family: "Gill Sans", "Gill Sans MT", "Myriad Pro", "DejaVu Sans Condensed", Helvetica, Arial, "sans-serif";
    margin: 2em;
}
h1 {
    font-size: 1.5em;
}
div {
    display: none;
}
#back-layer {
    background: url('kompv2-ui-entities.svg') no-repeat;
    background-size: 100% 100%;
    width: 800px;
    height: 800px;
    display: block;
}
div[id^="d"] {
    position: absolute;
    top: 140px;
}
div[id^="d"] span {
    width: 770px;
    display: block;
    height: 800px;
    margin-left: 30px;
}
</style>
</head>

<body>
<h1> Entities relationships diagram Kompv2 </h1>
<br>
<input name="pagetype" type="radio" onclick="show(0)" />
Allocation
<input name="pagetype" type="radio" onclick="show(1)" />
Availability manager
<input name="pagetype" type="radio" onclick="show(2)" />
Capacity Monitor
<input name="pagetype" type="radio" onclick="show(3)" />
KiwiSquare (Pre-qualification calcualtor)
<input name="pagetype" type="radio" onclick="show(4)" />
Surveyor
<input name="pagetype" type="radio" onclick="show(5)" />
None
<p></p>
<hr>
<br>
<span id="back-layer"> </span>
<div id="d0" class="CF" style="display:none;">
	<span style="background:url(allocation1.svg) no-repeat;"> </span> 
  <!--<p></p>
    <input name="pagetype" type="radio" onclick="show(3)" />One
    <input name="pagetype" type="radio" onclick="show(4)" />Two
    <input name="pagetype" type="radio" onclick="show(5)" />Three
    <input name="pagetype" type="radio" onclick="show(6)" />Four
    <input name="pagetype" type="radio" onclick="show(7)" />Five
    <input name="pagetype" type="radio" onclick="show(8)" />Six
    <input name="pagetype" type="radio" onclick="show(9)" />Seven--> 
</div>
<div id="d1">
	<span style="background:url(availability.svg) no-repeat;"> </span> 
	</div>
<div id="d2">
	<span style="background:url(capacitymonitor.svg) no-repeat;"></span></div>
<div id="d3"><span style="background:url(kiwisquare.svg) no-repeat;"></span></div>
<div id="d4"><span style="background:url(surveyour.svg) no-repeat;"></span></div>
<div id="d5"><span></span></div>

</body>
</html>
<script language="javascript">
function show(number) {
    
    $('[id^="d"]').hide();
    if(number >=6){
       $('#d0').show();
    }
    $('#d' + number).show();
}
</script>
