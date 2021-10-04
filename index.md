<html>
<head>

<!-- Remember to include jQuery :) -->
<meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

<link rel="stylesheet" type="text/css" href="ResponsiveTable.css">
<script>
	function createtable()
	{
		$('#eachTable').html("");
		var rows = $('#rows').val();
		if(rows=="")
		{
			alert("Please Select Number.");
			$('#eachTable').html("");
			return;
		}

		var eTable = '<div class="wrapper">';
		eTable += '<div class="table">';
		eTable += '<div class="row header green">'
			      +'<div class="cell">Name</div>'
			      +'<div class="cell">Age</div>'
			      +'<div class="cell">Gender</div>'
			      +'<div class="cell">Dob</div>'
			      +'<div class="cell">Action</div>'
			      +'</div>';

		for(var sl=1; sl<=rows; sl++)
		{

			eTable += '<div class="row">';
			eTable += '<div class="cell" data-title="Name"><input type="text"/></div>';
			eTable += '<div class="cell" data-title="Age"><input type="number"/></div>';
			eTable += '<div class="cell" data-title="Gender"><select id="gender" name="gender">'
					+'<option>Select</option>'
					+'<option>Male</option>'
					+'<option>Female</option>'
					+'</select></div>';
			eTable += '<div class="cell" data-title="Dob"><input type="date" name="dob" id="dob"/></div>';
			eTable += '<div class="cell" data-title="Action"><input type="submit" name="btnsubmit" id="btnsubmit" value="Click Here" class="btn btn-danger"/></div>';
			eTable += '</div>';
		}

		eTable += "</div></div>";
		$('#eachTable').html(eTable);
	}

</script>


</head>

<body class="bodyclass">
	How many row:-
	<select id="rows" onchange="createtable()">
		<option>Select</option>
		<option>1</option>
		<option>2</option>
		<option>3</option>
		<option>4</option>
		<option>5</option>
		<option>6</option>
	</select>
	<br/><br/>
	<div id="eachTable"></div>

</body>
<script src="jquery.min.js"></script>
</html>
