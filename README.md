<!DOCTYPE html>
<html lang="vi">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Quản Lý Kho Hàng</title>

    <style>

        *{
            margin:0;
            padding:0;
            box-sizing:border-box;
            font-family:Arial;
        }

        body{
            background:#f4f4f4;
            padding:30px;
        }

        .container{
            width:700px;
            margin:auto;
            background:white;
            padding:20px;
            border-radius:10px;
            box-shadow:0 0 10px rgba(0,0,0,0.1);
        }

        h1{
            text-align:center;
            margin-bottom:20px;
            color:#333;
        }

        .box{
            display:flex;
            gap:20px;
        }

        .menu{
            width:40%;
        }

        .menu h3{
            margin-bottom:10px;
        }

        .menu ul{
            list-style:none;
        }

        .menu li{
            background:#007bff;
            color:white;
            padding:12px;
            margin-bottom:10px;
            border-radius:5px;
            cursor:pointer;
        }

        .menu li:hover{
            background:#0056b3;
        }

        .info{
            width:60%;
            background:#f0f8ff;
            padding:20px;
            border-radius:10px;
        }

        .info h3{
            margin-bottom:15px;
        }

        .info p{
            margin-bottom:10px;
            font-size:18px;
        }

    </style>

</head>

<body>

    <div class="container">

        <h1>Quản Lý Kho Hàng</h1>

        <div class="box">

            <div class="menu">

                <h3>Thư mục sản phẩm</h3>

                <ul>

                    <li onclick="showInfo('Bút')">
                        Bút
                    </li>

                    <li onclick="showInfo('Thước kẻ')">
                        Thước kẻ
                    </li>

                    <li onclick="showInfo('Giấy')">
                        Giấy
                    </li>

                    <li onclick="showInfo('Compa')">
                        Compa
                    </li>

                    <li onclick="showInfo('Tẩy')">
                        Tẩy
                    </li>

                    <li onclick="showInfo('Máy tính')">
                        Máy tính
                    </li>

                </ul>

            </div>

            <div class="info" id="productInfo">

                <h3>Thông tin sản phẩm</h3>

                <p>Chọn sản phẩm để xem thông tin</p>

            </div>

        </div>

    </div>

    <script>

        const products = {

            "Bút": {
                quantity: 120,
                importDate: "12/05/2026",
                price: "5.000 VNĐ"
            },

            "Thước kẻ": {
                quantity: 50,
                importDate: "15/05/2026",
                price: "10.000 VNĐ"
            },

            "Giấy": {
                quantity: 300,
                importDate: "10/05/2026",
                price: "2.000 VNĐ"
            },

            "Compa": {
                quantity: 25,
                importDate: "08/05/2026",
                price: "20.000 VNĐ"
            },

            "Tẩy": {
                quantity: 70,
                importDate: "18/05/2026",
                price: "3.000 VNĐ"
            },

            "Máy tính": {
                quantity: 15,
                importDate: "20/05/2026",
                price: "150.000 VNĐ"
            }

        };

        function showInfo(product){

            const info = products[product];

            document.getElementById("productInfo").innerHTML = `

                <h3>Thông tin sản phẩm</h3>

                <p>
                    <b>Tên sản phẩm:</b>
                    ${product}
                </p>

                <p>
                    <b>Số lượng:</b>
                    ${info.quantity}
                </p>

                <p>
                    <b>Ngày nhập:</b>
                    ${info.importDate}
                </p>

                <p>
                    <b>Giá sản phẩm:</b>
                    ${info.price}
                </p>

            `;
        }

    </script>

</body>

</html>
