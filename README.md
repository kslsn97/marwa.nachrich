# marwa.nachrich
<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>marwa.nachricht</title>
  <style>
    #geheimtext {
      display: none;
      font-size: 24px;
      color: red;
      margin-top: 20px;
    }
  </style>
</head>
<body>
  <h2>Gib den 6-stelligen Code ein (z. B. 2,5,9,4,10,15):</h2>
  <input type="text" id="code" placeholder="Code eingeben">
  <button onclick="prüfen()">Bestätigen</button>

  <div id="geheimtext">ich liebe dich</div>

  <script>
    function prüfen() {
      const richtig = ["2", "5", "9", "4", "10", "15"];
      const eingabe = document.getElementById("code").value
        .split(",")
        .map(x => x.trim());

      if (eingabe.length === 6 && richtig.every((wert, i) => eingabe[i] === wert)) {
        document.getElementById("geheimtext").style.display = "block";
      } else {
        alert("Falscher Code!");
      }
    }
  </script>
</body>
</html>
