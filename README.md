<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تطبيق تعليم الرسم</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: #f0f0f0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 10px 0;
        }
        .content {
            padding: 20px;
        }
        .lesson {
            background-color: white;
            margin: 10px auto;
            padding: 20px;
            max-width: 600px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body>
    <header>
        <h1>تطبيق تعليم الرسم</h1>
    </header>
    <div class="content">
        <div class="lesson">
            <h2>درس 1: رسم الأشكال الأساسية</h2>
            <p>تعلم كيفية رسم الأشكال الأساسية مثل الدائرة والمربع والمثلث.</p>
            <canvas id="canvas" width="300" height="300" style="border:1px solid #000;"></canvas>
            <br>
            <button onclick="drawShapes()">ارسم الأشكال</button>
        </div>
    </div>
    <script>
        function drawShapes() {
            const canvas = document.getElementById('canvas');
            const ctx = canvas.getContext('2d');

            // رسم دائرة
            ctx.beginPath();
            ctx.arc(150, 70, 50, 0, Math.PI * 2);
            ctx.stroke();

            // رسم مربع
            ctx.beginPath();
            ctx.rect(100, 150, 100, 100);
            ctx.stroke();

            // رسم مثلث
            ctx.beginPath();
            ctx.moveTo(150, 270);
            ctx.lineTo(100, 370);
            ctx.lineTo(200, 370);
            ctx.closePath();
            ctx.stroke();
        }
    </script>
</body>
</html>
