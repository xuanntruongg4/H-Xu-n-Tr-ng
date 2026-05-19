<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bài tập jQuery Ẩn/Hiện</title>

    <style>
        body{
            font-family: Arial, sans-serif;
            margin: 40px;
        }

        h2{
            color: #333;
        }

        button{
            padding: 10px 20px;
            margin-right: 10px;
            border: 1px solid #999;
            background: white;
            cursor: pointer;
        }

        #box{
            width: 320px;
            padding: 20px;
            margin-top: 20px;
            border: 2px solid #4a90e2;
            background: #eaf4ff;
        }

        #box h3{
            margin-top: 0;
        }
    </style>
</head>
<body>

    <h2>Bài tập jQuery Ẩn / Hiện nội dung</h2>

    <button onclick="anNoiDung()">Ẩn nội dung</button>
    <button onclick="hienNoiDung()">Hiện nội dung</button>
    <button onclick="anHien()">Ẩn / Hiện</button>

    <div id="box">
        <h3>Thông báo</h3>
        <p>Đây là nội dung được điều khiển bằng jQuery.</p>
    </div>

    <script>
        function anNoiDung(){
            document.getElementById("box").style.display = "none";
        }

        function hienNoiDung(){
            document.getElementById("box").style.display = "block";
        }

        function anHien(){
            let box = document.getElementById("box");

            if(box.style.display === "none"){
                box.style.display = "block";
            } else {
                box.style.display = "none";
            }
        }
    </script>

</body>
</html>
