<!DOCTYPE html>
<html lang="tg">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Ҳисоби маблағҳо 3</title>
<style>
*{box-sizing:border-box}
body{
 font-family:Arial,sans-serif;
 background:#f1f5f9;
 margin:0;padding:15px;color:#1e293b
}
.container{max-width:600px;margin:auto}
header{
 background:#14532d;color:white;
 padding:20px;border-radius:14px;
 text-align:center;margin-bottom:15px
}
.card{
 background:white;padding:16px;
 border-radius:12px;margin-bottom:13px;
 box-shadow:0 2px 7px #0001
}
input,select,button{
 width:100%;padding:12px;margin:6px 0;
 border:1px solid #cbd5e1;
 border-radius:8px;font-size:16px
}
button{
 background:#15803d;color:white;
 border:0;font-weight:bold;cursor:pointer
}
.red{background:#dc2626}
.blue{background:#2563eb}
.orange{background:#ea580c}
.hidden{display:none}
.stat{
 display:flex;justify-content:space-between;
 padding:10px;border-bottom:1px solid #eee
}
.item{
 padding:12px;background:#f8fafc;
 border-radius:8px;margin:8px 0;
 border-left:4px solid #15803d
}
.small{font-size:13px;color:#64748b}
</style>
</head>
<body>
<div class="container">

<header>
<h2>ҲИСОБИ МАБЛАҒҲО</h2>
<p>Ҳисоботи ҳамсинфон</p>
</header>

<div id="login" class="card">
<h3>Воридшавӣ</h3>
<select id="role">
<option value="admin">Администратор</option>
<option value="cashier">Хазинадор</option>
</select>
<input id="password" type="password" placeholder="Рамзи воридшавӣ">
<button onclick="login()">Даромадан</button>
<p class="small">Администратор: 1111 | Хазинадор: 2222</p>
</div>

<div id="app" class="hidden">

<div class="card">
<h3>📊 Ҳисоботи умумӣ</h3>
<div class="stat"><span>Ҳамагӣ ворид шуд:</span><b id="totalIn">0</b></div>
<div class="stat"><span>Хароҷот:</span><b id="totalOut">0</b></div>
<div class="stat"><span>Бақияи умумӣ:</span><b id="balance">0</b></div>
<div class="stat"><span>Чекҳои интизори тасдиқ:</span><b id="pending">0</b></div>
</div>

<div class="card">
<h3>👥 Ҳамсинфон</h3>
<div id="people"></div>
<div id="adminAdd">
<input id="newName" placeholder="Номи ҳамсинф">
<button onclick="addPerson()">+ Илова кардани ҳамсинф</button>
</div>
</div>

<div class="card">
<h3>💰 Сабти маблағ</h3>
<select id="person"></select>
<input id="amount" type="number" placeholder="Маблағ (сомонӣ)">
<input id="description" placeholder="Шарҳ">
<button onclick="addIncome()">Сабти маблағ</button>
</div>

<div class="card">
<h3>➖ Сабти хароҷот</h3>
<input id="expenseAmount" type="number" placeholder="Маблағ (сомонӣ)">
<input id="expenseReason" placeholder="Сабаби хароҷот">
<button class="orange" onclick="addExpense()">С