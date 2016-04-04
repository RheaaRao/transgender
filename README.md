# transgender
Trangender Latinas' fight to end discrimination

Our newspeg was increased crimes against transgender Latinas/os in New York. So we checked census data and clips on Lexis Nexis to find 
more information about this. There is no census data but plenty of data collected through surveys by non-profits. We found an organization called Make the road that supports the low-income Latino community. We found people through their weekly meeting. We interviewed them in person, over the phone and email. They reffered us to healthcare services, law projects and found some through the leadership directory. 

Graphs were created using infogr.am. We used jquery (the text function) and javascript to create variables and then a for loop that manipulates certain elements in a sentence about healthcare and keeps changing every 1.5 seconds. The code is below. The index starts at 1 so the same sentence isn't inserted twice. 

<!DOCTYPE html>
<html>

<head>
  <title> health </title>
  
</head>

<body>

  <p>"Transgender Latina immigrants are <span id="number"> <em> 57% </em> </span> more likely to <span id= "changeone"> <em> inject themselves with harmful, unknown, appearance enhancing substances </em> </span> than see a doctor" </p>
  <p id = "data"> data by the TransLatin@ Coalition's project TransVisble(2014) </p>


  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.3/jquery.min.js"></script>
  <script>
  $(document).ready(function(){
 
   $('p').css('font-family', 'monospace');
   $('p').css('font-size', '30px');
   $('#number').css('font-size', '30px');
   $('#number').css('color', 'Red');
   $('#changeone').css('color', 'Red');
   $('#data').css('font-size', '12px');

	var stats= ["57%", "61%", "23%", "13%", "21%"],
		changes= ["inject themselves with harmful, unknown substances", "visit the emergency room", "self-diagnose at a pharmacy", "see what a friend recommends", "wait for the condition to go away"],
		i = 1;

	
	function changeSentence(i, m){

		$("#number").text(stats[i]);
		$("#changeone").text(changes[i]);

		if(i < m){
			setTimeout(function(){
				changeSentence(i+1, m);
			}, 1500);
		} else{
			changeSentence(0, m);

		}

	}

	changeSentence(i, stats.length);




});

  </script>


</body>

</html>
