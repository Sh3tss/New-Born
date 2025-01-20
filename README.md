<!doctype html>
<html>
	<head>
		<title>Calculadora com JS</title>
		<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
	</head>
	<body class="container">
		<form class="form m-2">
			<label class="form-label">Valor A</label> <input class="form-control" type="number" id="v1"/>
			<label class="form-label">Valor B</label> <input class="form-control" type="number" id="v2"/>
			<label class="form-label">Operação</label> <select class="form-select" id="oper"> 
				<option>Soma</option> <option>Subtração</option> <option>Multiplicação</option> <option>Divisão</option> <option>Potência</option></select>
			<a href="#" class="btn btn-primary m-2" 
				onclick="executar()">Executar</a>
		</form>
		<div class="alert alert-sucess" id="resp">
			O resultado aparecerá aqui!</div>
		<script src="Calculator.js"></script>
		<script>
			const executar=()=>{
				const a = eval(document.getElementById("v1").value);
				const b = eval(document.getElementById("v2").value);
				let oper = eval(document.getElementById("oper").selectedIndex);
				let resultado = (oper==0)?somar(a,b):(oper==1)?subtrair(a,b):(oper==2)?multiplicar(a,b):(oper==3)?dividir(a,b):exponencial(a,b);document.getElementById("resp").innerHTML=`O resultado da operação é ${resultado}`;
			}
		</script>
	</body>
</html>
