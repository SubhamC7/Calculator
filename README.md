# Calculator
It's a basic Calculator with few advanced features.. Try it!!
<!DOCTYPE html>
	<html lang="en">

	<head>
		<meta charset="UTF-8">
		<meta http-equiv="X-UA-Compatible" content="IE=edge">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">

		<title>calculator</title>

	</head>
		
		<body>

			<div class="calc">

		    <div class="solar"></div>
		
		    <div class="casio"> CASIO</div>


				<div class="display">
					<input type="text" id="result" maxlength=15 v-model="first_data"> {{first_data}}</input>
		
				</div>
		

				<div class="cal-body">

					<div>
						<button id="sym_btn" @click="clear();"> C </button>
						<button id="sym_btn" @click= "func_ip('Mod');"> Mod </button>
						<button id="sym_btn" @click= "func_ip('rt');"> rt </button>
						<button id="sym_btn" @click= "func_ip('sq');"> sq </button>
						<button id="sym_btn" @click= "sym_ip(' / ');"> / </button>

		      </div>
		
					<div>
						<button id="num_btn" value="7" @click= "number_ip('7');"> 7 </button>
						<button id="num_btn" value="8" @click= "number_ip('8');"> 8 </button>
						<button id="num_btn" value="9" @click= "number_ip('9');"> 9 </button>
						<button id="sym_btn" @click= "sym_ip(' x ');"> * </button>

		      </div>
		
					<div>
          	<button id="num_btn" value="4" @click= "number_ip('4');"> 4 </button>
						<button id="num_btn" value="5" @click= "number_ip('5');"> 5 </button>
						<button id="num_btn" value="6" @click= "number_ip('6');"> 6 </button>
						<button id="sym_btn" @click= "sym_ip(' - ');"> - </button>

		      </div>
		
					<div>
						<button id="num_btn" value="1" @click= "number_ip('1');"> 1 </button>
						<button id="num_btn" value="2" @click= "number_ip('2');"> 2 </button>
						<button id="num_btn" value="3" @click= "number_ip('3');"> 3 </button>
						<button id="sym_btn" @click= "sym_ip(' + ');"> + </button>

		      </div>
		
					<div>
			      <button id="num_btn" value="0" @click= "number_ip('0');"> 0 </button>
			      <button id="sym_btn" style="width:50px" @click= "dot_ip('.');"> . </button>
						<button id="sym_btn" style="width:50px" @click= "del"> DEL </button>
						<button id="sym_btn" style="width:50px" @click= "sym_ip(' % ');"> % </button>
						<button id="sym_btn" class="equal" @click= "show();" style="width:60px; background-color: rgba(212, 185, 29, 0.979);"> = </button>

		      </div>
		
		
				</div>
		
			</div>
		
		</body>
		
	</html>
  
  
  
  
  
  
  
  
  style
		* {
			margin: 0%;
			padding: 0%;
			box-sizing: border-box;
		}

		.calc 
    {
			height: 520px;
			max-width: 310px;
			margin: 0 auto;
			text-align: center;
			margin-top: 25px;
			box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.3);
			transition: 0.3s;
			font-size: 0;
			background-color: rgba(4, 99, 75, 0.418);
			padding-top: 10px;
			border-radius: 20px;
			border: rgba(13, 93, 117, 0.644) solid;
		}

    .solar
    {
      margin-left:210px;
      height: 25px;
      width: 80px;
      border-radius: 7px;
      background-color: rgba(114, 25, 25, 0.658);
      border-color: rgb(0, 9, 12) solid;
    }

    .calc .casio
    {
			background-color: rgba(13, 93, 117, 0.644) solid;
      margin-top: 0px;
      align-items: center;
      font-size: 25px;
    }

		.calc:hover 
    {
			box-shadow: 0 16px 32px 0 rgba(0, 0, 0, 0);
		}


		.display #result 
    {
      margin-top: 25px;
			height: 110px;
			width: 272px;
			font-size: 25px;
			font-weight: bold;
			text-align: right;
			padding: 0 10px;
			background-color: rgba(50, 61, 71, 0.795);
			border-radius: 10px;
		}

		.cal-body 
    {
			margin-top: 20px;

		}

    .cal-body #sym_btn 
    {
    	margin-top: 10px;
      margin-right: 2px;
			background-color: rgba(20, 38, 202, 0.699);
      height: 45px;
			width: 57px;
      font-size: 20px;
      border-radius: 7px;
			font-family: Impact, 'Arial Narrow Bold', sans-serif;
      margin-bottom: 0.5px;
		}

		.cal-body #num_btn 
    {
      margin-top: 10px;
      margin-right: 2px;
			height: 45px;
			width: 77px;
			font-size: 20px;
			font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
			font-weight: bold;
			border-radius: 7px;
			background-color: rgba(233, 101, 61, 0.986);
			color: rgba(0, 0, 0, 0.74);
		}




		.cal-body #num_btn:hover {
			background-color: rgba(230, 23, 23, 0.918);
		}

    .cal-body #sym_btn:hover {
			background-color: rgba(230, 23, 23, 0.918);
		}
