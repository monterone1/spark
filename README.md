[test-ios.html](https://github.com/user-attachments/files/30246068/test-ios.html)
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
body{font-family:sans-serif;padding:40px;background:#f5f5f5;}
.btn{display:block;width:100%;padding:20px;background:#E8445A;color:#fff;border:none;border-radius:16px;font-size:18px;font-weight:700;margin-bottom:16px;cursor:pointer;}
.result{padding:16px;background:#fff;border-radius:12px;font-size:16px;min-height:60px;}
</style>
</head>
<body>
<h2>Тест кнопок на iOS</h2>

<button class="btn" onclick="test('onclick сработал!')">Тест onclick</button>
<button class="btn" id="btn2">Тест addEventListener</button>
<div class="btn" onclick="test('div onclick сработал!')" style="text-align:center">Тест div onclick</div>

<div class="result" id="result">Нажми кнопку — покажет результат</div>

<script>
function test(msg){
  document.getElementById('result').textContent = msg + ' в ' + new Date().toLocaleTimeString();
}
document.getElementById('btn2').addEventListener('click', function(){
  test('addEventListener сработал!');
});
</script>
</body>
</html>
