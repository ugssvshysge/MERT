<!DOCTYPE html><html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>إدخال بيانات البوت</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            direction: rtl;
        }
        input, button {
            margin: 10px;
            padding: 10px;
        }
    </style>
</head>
<body>
    <h2>أدخل بيانات البوت</h2>
    <label for="token">توكن البوت:</label>
    <input type="text" id="token" placeholder="أدخل التوكن هنا">
    <br>
    <label for="telegramId">ايدي تيليجرام:</label>
    <input type="text" id="telegramId" placeholder="أدخل الايدي هنا">
    <br>
    <button onclick="submitData()">إرسال</button>
    <p id="output"></p><script>
    function submitData() {
        let token = document.getElementById('token').value;
        let telegramId = document.getElementById('telegramId').value;
        
        if (token === '' || telegramId === '') {
            alert('يرجى ملء جميع الحقول');
            return;
        }
        
        document.getElementById('output').innerText = `توكن البوت: ${token}\nايدي تيليجرام: ${telegramId}`;
    }
</script>

</body>
</html>
