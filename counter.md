---
layout: null
permalink: /tools/corona-carrom-counter/
---
<html>
<head>
	<!-- Required meta tags -->
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

	<!-- Bootstrap CSS -->
	<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
	<style>
		.bd-placeholder-img {
			font-size: 5.125rem;
			text-anchor: middle;
			-webkit-user-select: none;
			-moz-user-select: none;
			-ms-user-select: none;
			user-select: none;
		}
		@media (min-width: 768px) {
			.bd-placeholder-img-lg {
				font-size: 3.5rem;
			}
		}
	</style>
	<script type="text/javascript">
		var counter = {
			missCount1: 0,
			missCount2: 0,
			missCount3: 0,
			missCount4: 0
		}
		function setCount(counterName) {
			document.getElementById(counterName).textContent=counter[counterName].toString().padStart(2, '0');
		}
		function initCounts() {
			setCount('missCount1');
			setCount('missCount2');
			setCount('missCount3');
			setCount('missCount4');
		}
		function increment(counterName) {
			counter[counterName]++;
			setCount(counterName);
		}
		function decrement(counterName) {
			counter[counterName]--;
			if (counter[counterName] < 0) {
				counter[counterName] = 0
			}
			setCount(counterName);
		}
		function resetCounter(counterName) {
			counter[counterName] = 0;
			setCount(counterName)
		}
	</script>
	<title>Corona Carrom Counter</title>
</head>
<body onload="initCounts()">
	<h1 class="text-center">Corona Carrom Counter</h1>

	<!-- jQuery first, then Popper.js, then Bootstrap JS -->
	<script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
	<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
	<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>

	<main role="main">
		<div class="Counter py-5 bg-light">
			<div class="container">
				<div class="row">
					<div class="col-md-5">
						<div class="card mb-5 shadow-sm">
							<button type="button" class="btn btn-lg btn-outline-light" onclick="increment('missCount1')">
								<svg class="bd-placeholder-img card-img-top" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice" focusable="true" role="img" aria-label="Placeholder: 00"><rect width="100%" height="100%" fill="#3672d9"/><text id="missCount1" x="50%" y="50%" fill="#eceeef" dy=".4em"></text></svg>
							</button>
							<div class="card-body">
								<div class="btn-grp align-items-center">
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="decrement('missCount1')">&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;</button>
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="resetCounter('missCount1')">Reset</button>
								</div>
							</div>
						</div>
					</div>
					<div class="col-md-5">
						<div class="card mb-4 shadow-sm">
							<button type="button" class="btn btn-lg btn-outline-light" onclick="increment('missCount2')">
								<svg class="bd-placeholder-img card-img-top" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: 00"><rect width="100%" height="100%" fill="#d6cf49"/><text id="missCount2" x="50%" y="50%" fill="#0f0f0f" dy=".4em"></text></svg>
							</button>
							<div class="card-body">
								<div class="btn-grp align-items-center">
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="decrement('missCount2')">&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;</button>
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="resetCounter('missCount2')">Reset</button>
								</div>
							</div>
						</div>
					</div>
				</div>
				<div class="row">
					<div class="col-md-5">
						<div class="card mb-4 shadow-sm">
							<button type="button" class="btn btn-lg btn-outline-light" onclick="increment('missCount3')">
								<svg class="bd-placeholder-img card-img-top" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: 00"><rect width="100%" height="100%" fill="#d06bf2"/><text id="missCount3" x="50%" y="50%" fill="#0f0f0f" dy=".4em"></text></svg>
							</button>
							<div class="card-body">
								<div class="btn-grp">
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="decrement('missCount3')">&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;</button>
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="resetCounter('missCount3')">Reset</button>
								</div>
							</div>
						</div>
					</div>
					<div class="col-md-5">
						<div class="card mb-4 shadow-sm">
							<button type="button" class="btn btn-lg btn-outline-light" onclick="increment('missCount4')">
								<svg class="bd-placeholder-img card-img-top" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="xMidYMid slice" focusable="false" role="img" aria-label="Placeholder: 00"><rect width="100%" height="100%" fill="#f5073b"/><text id="missCount4" x="50%" y="50%" fill="#eceeef" dy=".4em"></text></svg>
							</button>
							<div class="card-body">
								<div class="btn-grp">
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="decrement('missCount4')">&nbsp;&nbsp;&nbsp;-&nbsp;&nbsp;&nbsp;</button>
									<button type="button" class="btn btn-lg btn-outline-primary" onclick="resetCounter('missCount4')">Reset</button>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</main>
</body>
</html>
