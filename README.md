<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>سایت سالن های سعدی</title>
    <link href="https://cdn.jsdelivr.net/gh/rastikerdar/sarbaz-font@v30.1.0/dist/font-face.css" rel="stylesheet" type="text/css" />
    <style>
        body {
            font-family: 'Sarbaz', sans-serif;
            margin: 0;
            padding: 0;
            overflow: hidden;
            color: #fff;
        }
        body::before {
            content: "";
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(120deg, #1e3c72, #2a5298, #76b852, #8dc26f);
            background-size: 400% 400%;
            animation: backgroundMove 10s infinite linear;
            z-index: -1;
        }
        @keyframes backgroundMove {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        h1 {
            font-size: 32px;
            text-align: right;
            padding: 20px;
            margin: 0;
            background-color: rgba(0, 0, 0, 0.7);
            animation: fadeIn 1.5s ease-in-out;
            color: #fff;
        }
        .container {
            display: flex;
            height: calc(100vh - 80px);
            overflow: hidden;
        }
        .sidebar {
            width: 25%;
            background-color: rgba(0, 0, 0, 0.8);
            padding: 10px;
            overflow-y: auto;
        }
        .content {
            width: 75%;
            padding: 20px;
            background-color: rgba(255, 255, 255, 0.8);
            overflow-y: auto;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.5);
            color: #000; /* رنگ متن محتوای هر هفته */
        }
        .week-list button {
            display: block;
            width: 100%;
            margin: 10px 0;
            padding: 10px;
            text-align: center;
            background-color: #28a745;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            transition: transform 0.3s, background-color 0.3s;
        }
        .week-list button:hover {
            background-color: #218838;
            transform: scale(1.05);
        }
        .photos img {
            width: 150px; /* افزایش اندازه تصاویر */
            height: 150px; /* افزایش ارتفاع تصاویر */
            margin: 10px; /* فضای بیشتر بین تصاویر */
            border-radius: 5px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.4);
            transition: transform 0.3s ease-in-out;
        }
        .photos img:hover {
            transform: rotate(10deg) scale(1.1);
        }
        footer {
            text-align: center;
            padding: 5px;
            background-color: rgba(0, 0, 0, 0.7);
            color: #fff;
            position: fixed;
            bottom: 0;
            width: 100%;
            font-size: 12px;
        }
        footer a {
            text-decoration: none;
            color: #ffc107;
            font-weight: bold;
            transition: color 0.3s;
        }
        footer a:hover {
            color: #fd7e14;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        @keyframes slideIn {
            from { transform: translateX(-100%); }
            to { transform: translateX(0); }
        }
        .week-content {
            animation: slideIn 0.5s ease-in-out;
        }
    </style>
</head>
<body>
    <h1>سایت سالن های سعدی</h1>
    <div class="container">
        <div class="sidebar">
            <div class="week-list">
                <button onclick="showWeek('week1')">تِست</button>
                <button onclick="showWeek('week2')">تِست</button>
                <button onclick="showWeek('week3')">تِست</button>
            </div>
        </div>
        <div class="content">
            <div id="week1" class="week-content" style="display: none;">
                <h2>١٤٠٣/٩/٢٥</h2>
                <p>سایت در حالت آزمایشی قرار دارد و تصاویر زیر تستی هستند</p>
                <div class="photos">
                    <img src="https://via.placeholder.com/150" alt="عکس 1">
                    <img src="https://via.placeholder.com/150" alt="عکس 2">
                    <img src="https://via.placeholder.com/150" alt="عکس 3">
                </div>
            </div>
            <div id="week2" class="week-content" style="display: none;">
                <h2>١٤٠٣/١٠/١</h2>
                <p>تست</p>
                <div class="photos">
                    <img src="https://via.placeholder.com/150" alt="عکس 4">
                    <img src="https://via.placeholder.com/150" alt="عکس 5">
                    <img src="https://via.placeholder.com/150" alt="عکس 6">
                </div>
            </div>
            <div id="week3" class="week-content" style="display: none;">
                <h2>١٤٠٣/١٠/١٠</h2>
                <p>تست</p>
                <div class="photos">
                    <img src="https://via.placeholder.com/150" alt="عکس 7">
                    <img src="https://via.placeholder.com/150" alt="عکس 8">
                    <img src="https://via.placeholder.com/150" alt="عکس 9">
                </div>
            </div>
        </div>
    </div>
    <footer>
        ساخته شده توسط <a href="https://serverqp.github.io/EnterAi" target="_blank">محمدجواد جاودانفرد</a>  👉کلیک کنید
   </footer>
    <script>
        function showWeek(weekId) {
            const contents = document.querySelectorAll('.week-content');
            contents.forEach(content => content.style.display = 'none');
            document.getElementById(weekId).style.display = 'block';
        }
    </script>
</body>
</html>
