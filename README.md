<!DOCTYPE html>
<html>
<body>
  <h2><b>Get your advice here</b></h2>
  <p id="advice"><b>Click the button below 👇</b></p>
  <p id="count"><b>You have read 0 advice today.</b></p>
  <button onclick="g()">Get Advice</button>
  <script>
    let c=0;
    function g(){
   fetch('https://api.adviceslip.com/advice')
   .then(r=>r.json())
  .then(d=>{
    advice.innerText=d.slip.advice.toUpperCase();
   count.innerText=`You have read ${++c} advice${c>1?'s':''} today.`;
      });
    }
</script>
</body>
</html>
