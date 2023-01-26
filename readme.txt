html-------------------------------------------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="app.css">
    <title>ILY</title>
</head>
<body>
    <div class="love">
        <input type="checkbox" hidden>
        <span></span>
        <span></span>
        <span></span>
        <p></p>
    </div>
</body>
</html>
css--------------------------------------------
body {
  background-color: black;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.love {
  position: relative;
  width: 50px;
  height: 50px;
}
p::after {
  position: absolute;
  width: 50px;
  height: 50px;
  content: "I LOVE";
  color: #000000;
  font-size: 8px;
  font-weight: bolder;
  top: 10px;
  left: 1px;
  transition: all 0.5s ease-in-out;
}
.love span {
  position: absolute;
  width: 30px;
  height: 30px;
  background-color: #00dd5f;
  transition: all 0.5s ease-in-out;
}
.love input {
  position: absolute;
  width: 50px;
  height: 50px;
  margin: 0;
  opacity: 0;
  cursor: pointer;
  z-index: 9;
}
.love input:checked-span:nth-child(2) {
  background-color: #d40000;
  border-radius: 50%;
  left: 0;
  z-index: 1;
  animation: effects 0.5s linear alternate;
}
.love input:checked-span:nth-child(3) {
  background-color: #d40000;
  border-radius: 50%;
  left: 20px;
  z-index: 1;
  animation: effects 0.5s linear alternate;
}
.love input:checked-span:nth-child(4) {
  background-color: #d40000;
  top: 10px;
  left: 10px;
  transform: rotate(45deg);
  transition: effects 0.5s linear alternate;
}
.love input:checked-p:after {
  content: "YOU";
  letter-spacing: 3px;
  color: #fff;
  z-index: 1;
  top: 10px;
  left: 13px;
}
@keyframes effects {
  100% {
    transform: rotate(360deg);
  }
}
