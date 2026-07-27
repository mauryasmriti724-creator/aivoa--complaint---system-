 <!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aivoa AI Complaint Generator</title>
<style>
  body { font-family: Arial; background:#f5f5f5; padding:20px; }
  .box { background:white; padding:20px; border-radius:10px; max-width:600px; margin:auto; box-shadow:0 2px 10px rgba(0,0,0,0.1); }
  h1 { color:#ff6b00; text-align:center; }
  label { font-weight:bold; margin-top:10px; display:block; }
  input, select, textarea { width:100%; padding:10px; margin:8px 0; border:1px solid #ccc; border-radius:5px; box-sizing:border-box; }
  button { background:#ff6b00; color:white; padding:15px; border:none; border-radius:8px; width:100%; font-size:16px; cursor:pointer; margin-top:10px; }
  button:hover { background:#e65c00; }
  #result { background:#eef; padding:15px; border-radius:8px; margin-top:15px; white-space:pre-wrap; border:1px solid #cce; }
</style>
</head>
<body>
<div class="box">
  <h1>AI Complaint Letter Generator</h1>
  <p>Aivoa platform ke liye complaint letter 10 second me banao</p>
  
  <label>Complaint Type:</label>
  <select id="type">
    <option>Service Issue</option>
    <option>Payment Problem</option>
    <option>Delivery Delay</option>
    <option>Other</option>
  </select>

  <label>Apna Naam:</label>
  <input type="text" id="name" placeholder="Apna naam likho">

  <label>Problem Detail:</label>
  <textarea id="problem" rows="4" placeholder="Problem detail me likho..."></textarea>

  <button onclick="generate()">AI Se Letter Banao</button>

  <div id="result"></div>
</div>

<script>
function generate() {
  let type = document.getElementById('type').value;
  let name = document.getElementById('name').value;
  let problem = document.getElementById('problem').value;
  
  if(name==="" || problem===""){ 
    alert("Naam aur Problem bharna zaroori hai"); 
    return; 
  }
  
  let letter = `Seva me,\nAivoa Support Team\nVishay: ${type} ke sambandh me shikayat\nMahoday,\n\nMera naam ${name} hai. Main Aivoa platform ka user hun. Mujhe ye samasya aa rahi hai: ${problem}\n\nKripya iska jald se jald samadhan karein. Main umeed karta/karti hun ki aap meri madad karenge.\n\nDhanyawad\n${name}`;
  
  document.getElementById('result').innerText = letter;
}
</script>
</body>
</html>
