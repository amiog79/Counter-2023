# Counter-2023
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title></title>
</head>
<style type="text/css">
	body {
  box-sizing: border-box;
  height: 100vh;
  font-family: sans-serif;
  display: grid;
  place-items: center;
  background: #a2c8ec;
}
.content {
  text-align: center;
  border: 4px solid #0d47a1;
  border-radius: 20px;
  padding: 5%;
}
h1 {
  margin: 0;
  text-transform: uppercase;
  font-size: 3rem;
  color: #0d47a1;
}
.value {
  font-size: 8rem;
  font-weight: bold;
  color: #455a64;
}

.btn {
  text-transform: uppercase;
  background: transparent;
  color: #0d47a1;
  padding: 0.4rem 0.8rem;
  display: inline-block;
  transition: all 0.5s linear;
  font-size: 0.9rem;
  font-weight: bold;
  border: 2px solid #0d47a1;
  border-radius: 5px;
  margin: 0.3rem;
  cursor: pointer;
}
.btn:hover {
  background: #0d47a1;
  color: #a2c8ec;
}
.decrease:hover {
  color: #f40;
}
.increase:hover {
  color: #390;
}

</style>

<body style="background: linear-gradient(45deg, red, yellow);">

	<div style="background: linear-gradient(45deg, white, violet);" class="content">
  <h1>Days Counter</h1>
  <span class="value">0</span>
  <div class="btn-wrap">
    <button class="btn decrease">decrease</button>
    <button class="btn reset" >reset</button>
    <button class="btn increase">increase</button>
  </div>
</div>

<script type="text/javascript">
	let count = 0;

const value = document.querySelector(".value");
const buttonsArr = document.querySelectorAll(".btn");

buttonsArr.forEach((btn) => {
  btn.addEventListener("click", (ev) => {
    const className = ev.currentTarget.classList;
    if (className.contains("decrease")) {
      count--;
    } else if (className.contains("increase")) {
      count++;
    } else {
      count = 0;
    }
    if (count < 0) {
      value.style.color = "#f40";
    } else if (count > 0) {
      value.style.color = "#390";
    } else {
      value.style.color = "#455a64";
    }
    value.textContent = count;
  });
});

</script>

</body>
</html>
