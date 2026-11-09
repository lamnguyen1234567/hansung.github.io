
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HOCHICKEN - Promotion A</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: Arial, sans-serif;
    background: #f5f5f5;
    color: #222;
    padding: 30px 15px;
}

.container {
    max-width: 550px;
    margin: auto;
}

.card {
    background: white;
    border: 1px solid #ddd;
    border-radius: 22px;
    overflow: hidden;
    box-shadow: 0 4px 15px rgba(0,0,0,0.06);
}

.product-image {
    width: 100%;
    height: 320px;
    object-fit: cover;
    display: block;
}

.content {
    padding: 30px;
}

.tag {
    display: inline-block;
    background: #e6f3fc;
    color: #438bb9;
    padding: 8px 17px;
    border-radius: 25px;
    font-size: 18px;
    margin-bottom: 25px;
}

h1 {
    font-size: 27px;
    margin-bottom: 20px;
}

.description {
    font-size: 21px;
    line-height: 1.7;
    margin-bottom: 25px;
}

ul {
    padding-left: 25px;
}

li {
    font-size: 21px;
    line-height: 2;
}

.note {
    color: #999;
    margin-top: 25px;
    font-size: 15px;
}

.experiment {
    background: white;
    padding: 25px;
    margin-top: 25px;
    border-radius: 18px;
}

.experiment h2 {
    margin-bottom: 20px;
}

select {
    width: 100%;
    padding: 14px;
    border: 1px solid #ddd;
    border-radius: 8px;
    font-size: 17px;
    margin: 15px 0;
}

.result {
    background: #fff7e9;
    padding: 20px;
    border-radius: 12px;
    line-height: 2.2;
}

.result strong {
    color: #e45b26;
}

button {
    width: 100%;
    padding: 14px;
    background: #ffb400;
    border: none;
    border-radius: 9px;
    font-size: 17px;
    font-weight: bold;
    cursor: pointer;
    margin-top: 18px;
}

</style>
</head>

<body>

<div class="container">

    <!-- PRODUCT PROMOTION CARD -->
    <div class="card">

        <img
            class="product-image"
            src="https://images.unsplash.com/photo-1626645738196-c2a7c87a8f58?w=900"
            alt="Fried Chicken"
        >

        <div class="content">

            <span class="tag">Phương án A</span>

            <h1>많이 살수록 더 큰 할인</h1>

            <p class="description">
                Mua càng nhiều, giảm càng nhiều.
            </p>

            <ul>
                <li>1 phần: Không giảm</li>
                <li>2 phần: Giảm 3.000 won</li>
                <li>3 phần: Giảm 6.000 won</li>
            </ul>

            <p class="note">
                할인 금액 증가형
            </p>

        </div>
    </div>

    <!-- EXPERIMENT -->
    <div class="experiment">

        <h2>Thử nghiệm tính giá</h2>

        <label>Chọn số lượng gà:</label>

        <select id="quantity" onchange="calculate()">
            <option value="1">1 phần</option>
            <option value="2">2 phần</option>
            <option value="3">3 phần</option>
            <option value="4">4 phần</option>
            <option value="5">5 phần</option>
        </select>

        <div class="result">

            <p>Giá gốc:
                <span id="original">20.000 won</span>
            </p>

            <p>Giảm giá:
                <strong id="discount">0 won</strong>
            </p>

            <p>Tổng thanh toán:
                <strong id="total">20.000 won</strong>
            </p>

        </div>

        <button onclick="calculate()">
            Tính giá khuyến mãi
        </button>

    </div>

</div>

<script>

function calculate() {

    const quantity = Number(
        document.getElementById("quantity").value
    );

    const price = 20000;

    // Tổng tiền ban đầu
    const original = quantity * price;

    // Cứ 2 phần được giảm 3.000 won
    const discount = Math.floor(quantity / 2) * 3000;

    // Tổng tiền sau giảm
    const total = original - discount;

    document.getElementById("original").innerText =
        original.toLocaleString("ko-KR") + " won";

    document.getElementById("discount").innerText =
        discount.toLocaleString("ko-KR") + " won";

    document.getElementById("total").innerText =
        total.toLocaleString("ko-KR") + " won";
}

calculate();

</script>

</body>
</html>
