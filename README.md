<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>平安咖啡抽獎</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            margin: 50px;
        }
        #gif-container {
            display: none;
            margin-top: 20px;
        }
        #result {
            display: none;
            font-size: 1.5em;
            margin-top: 20px;
        }
        button {
            font-size: 1.2em;
            padding: 10px 20px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <h1>試試好手氣，平安咖啡抽回家</h1>
    <button onclick="startLottery()">抽獎</button>
    <div id="gif-container">
        <img id="gif" src="媽祖GIF.gif" alt="抽獎動畫" width="300">
    </div>
    <div id="result"></div>

    <script>
        function startLottery() {
            document.getElementById("result").style.display = "none";
            document.getElementById("gif-container").style.display = "block";
            
            setTimeout(() => {
                document.getElementById("gif-container").style.display = "none";
                
                const prizes = [
                    "恭喜中獎媽祖濾掛咖啡一包",
                    "恭喜中獎虎爺濾掛咖啡一包",
                    "恭喜中獎媽祖、虎爺濾掛咖啡各一包",
                    "恭喜中獎媽祖濾掛咖啡二包",
                    "恭喜中獎虎爺濾掛咖啡二包"
                ];
                const result = prizes[Math.floor(Math.random() * prizes.length)];
                
                document.getElementById("result").innerText = result;
                document.getElementById("result").style.display = "block";
            }, 5000);
        }
    </script>
</body>
</html>
