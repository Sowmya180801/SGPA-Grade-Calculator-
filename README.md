# SGPA-Grade-Calculator
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width", initial-scale=1.0">
    <title>Grade Calculator of SGPA</title>
    <style>
        .sub{
            padding:15px;
            margin:3px;
            border-radius: 4px;
        }
        .credits{
            padding:15px;
            margin:3px;
            border-radius: 4px;
        }
        .btn{
            padding-left:30px;
            padding-right:30px;
            padding-top:10px;
            padding-bottom:10px;
            margin:5px;
            border-radius: 8px;
            color: rgb(6, 155, 68); 
            background-color: green; 
            display: block;
            color: white;
            border: none;
            margin: 20px auto;
        }
        .grade{
            width: 100%;
            margin:0 auto;
            background-color: rgb(112, 197, 218);
            display: flex;
            justify-content: center;
            flex-direction: column;
            align-items: center;
        }
    </style>
</head>
<body bgcolor="whitesmoke">
    <div class="grade">
  <h1>SGPA Calculator</h1>
  <div>
    <input  class="sub" placeholder="enter sub1" />
    <input class="credits" placeholder="credits1" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub2" />
    <input class="credits" placeholder="credits2" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub3" />
    <input class="credits" placeholder="credits3" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub4" />
    <input class="credits" placeholder="credits4" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub5" />
    <input class="credits" placeholder="credits5" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub6" />
    <input class="credits" placeholder="credits6" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub7" />
    <input class="credits" placeholder="credits7" />
  </div>
  <div>
    <input class="sub" placeholder="enter sub8" />
    <input class="credits" placeholder="credits8" />
  </div>
  <button onclick="getResult()" class="btn">Calculate</button>
</div>
</body>
<script>
    let marks = [];
    let credits = [];
    function getResult() {
    let all_marks = Array.from(document.querySelectorAll(".sub"));
    all_marks.forEach((node) => {
    marks.push(node.value);
    });
    let all_credits = Array.from(document.querySelectorAll(".credits"));
    all_credits.forEach((node) => {
    credits.push(node.value);
    });
    let sum = 0;
    let total_credits = 0;
    for(let i = 0;i < 8;i++){
        sum = sum + marks[i] * credits[i];
        total_credits += parseInt(credits[i]);
    }
    const h1 = document.createElement("h1");
    h1.innerText = sum /total_credits;
    h1.style.textAlign = "center";
    document.body.append(h1);
}
</script>
</html>
