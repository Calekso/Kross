Kross
=====
<script type = "text/javascript">
 var check = false;
     m = 0;
 
 function fin(res) {
 var i = 1;
 for (i=1; i<=9; i++) { 
	kross[i] = res; 
	document.getElementById(i).value = res; 
	document.getElementById(i).disabled="disabled";
 	}
 }
	 
 function res(ids) {
	  
	if (check == true)
		{kross[ids]="O"; document.getElementById(ids).value = "O";document.getElementById(ids).disabled="disabled"; check = false; m++}
	else { if ( check == false) 
		{kross[ids]="X"; document.getElementById(ids).value = "X ";document.getElementById(ids).disabled="disabled"; check = true; m++}}
	 

	
	 
		if (kross[1] == kross[2])
			{if ( kross[1] == kross[3]) 
					{alert('"'+kross[1]+'" win!'); 
					fin(kross[1])}} 
		else {
			if (kross[1] == kross[5])
				{if ( kross[1] == kross[9]) 
					{alert('"'+kross[1]+'" win!'); 
					fin(kross[1])}} 
			else {
				if (kross[1] == kross[4])
					{if ( kross[1] == kross[7]) 
						{alert('"'+kross[1]+'" win!'); 
						fin(kross[1])}}   
				else {
	 
					if (kross[5] == kross[4])
						{if ( kross[5] == kross[6]) 
							{alert('"'+kross[5]+'" win!'); 
							fin(kross[5])}} 
					else {
						if (kross[5] == kross[3])
							{if ( kross[5] == kross[7]) 
								{alert('"'+kross[5]+'" win!'); 
								fin(kross[5])}} 
						else {
							if (kross[5] == kross[2])
								{if ( kross[5] == kross[8]) 
									{alert('"'+kross[5]+'" win!'); 
									fin(kross[5])}}   
							else {
	 
								if (kross[9] == kross[8])
									{if ( kross[9] == kross[7]) 
										{alert('"'+kross[9]+'" win!'); 
										fin(kross[9])}} 
								else {
									if (kross[9] == kross[6])
										{if ( kross[9] == kross[3]) 
											{alert('"'+kross[9]+'" win!'); 
											fin(kross[9])}}
	 
	 
	 }}}}}}}
	 if (m == 9) {alert("Game over")}
	 }
 
 var kross = new Array("0","1","2","3","4","5","6","7","8","9") ;
	
	document.write('<table border=1><tr><td>	<input id=1 type="button" value="   " onClick=res(id)>');
	document.write('<td> <input id=2 type="button" value="   " onClick=res(id)>');
	document.write('<td> <input id=3 type="button" value="   " onClick=res(id)>');
	document.write('<tr><td><input id=4 type="button" value="   " onClick=res(id)>');
	document.write('<td> <input id=5 type="button" value="   " onClick=res(id)>');
	document.write('<td> <input id=6 type="button" value="   " onClick=res(id)>');
	document.write('<tr><td><input id=7 type="button" value="   " onClick=res(id)>');
	document.write('<td> <input id=8 type="button" value="   " onClick=res(id)>');
	document.write('<td> <input id=9 type="button" value="   " onClick=res(id)>');
	document.write("</table>");

 
</script>
