<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>오늘의 할인 쿠폰</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, "Noto Sans KR", sans-serif;
    background: #f5f5f5;
    color: #222;
}

/* 메인 페이지 */
.header {
    background: white;
    padding: 25px 20px;
    font-size: 25px;
    font-weight: bold;
}

.search {
    margin: 15px 20px;
    padding: 16px;
    border: 1px solid #ddd;
    border-radius: 30px;
    background: white;
    color: #999;
}

.banner {
    margin: 20px;
    padding: 35px 20px;
    background: #e9e5ff;
    border-radius: 15px;
    font-size: 25px;
    font-weight: bold;
    color: #5332a8;
}

.categories {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
    padding: 25px 15px;
    background: white;
    text-align: center;
}

.category {
    font-size: 14px;
}

.category span {
    display: block;
    font-size: 32px;
    margin-bottom: 8px;
}

.foods {
    padding: 25px 15px;
}

.food-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
}

.food {
    background: white;
    border-radius: 12px;
    padding: 12px;
}

.food-image {
    height: 120px;
    background: #ffe6ca;
    border-radius: 10px;
    display: grid;
    place-items: center;
    font-size: 55px;
}

.food p {
    margin-top: 10px;
    font-weight: bold;
}

/* 배경 어둡게 */
.overlay {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.62);
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 10;
    padding: 15px;
}

/* 팝업 전체 */
.popup {
    position: relative;
    width: 100%;
    max-width: 600px;
    text-align: center;
}

/* 닫기 버튼 */
.close {
    position: absolute;
    right: 0;
    top: -48px;
    width: 48px;
    height: 48px;
    border: none;
    border-radius: 50%;
    background: white;
    font-size: 30px;
    cursor: pointer;
    z-index: 5;
}

/* 주황색 할인 배너 */
.orange {
    width: 88%;
    margin: auto;
    min-height: 500px;
    background: #ff4b0b;
    color: white;
    padding: 110px 15px 100px;
    clip-path: polygon(13% 0, 100% 0, 88% 58%,
    100% 58%, 83% 100%, 0 83%);
    transform: rotate(-3deg);
}

.orange h2 {
    color: #501900;
    font-size: clamp(32px, 8vw, 55px);
    font-weight: 900;
    font-style: italic;
}

.orange .amount {
    font-size: clamp(55px, 13vw, 95px);
    font-weight: 900;
    font-style: italic;
    white-space: nowrap;
    margin: 10px 0;
}

.orange .sale {
    color: #641d00;
    font-size: 55px;
    font-weight: 900;
    text-align: right;
    padding-right: 25px;
}

/* 쿠폰 */
.ticket {
    position: relative;
    margin: -20px auto 0;
    width: 75%;
    height: 160px;
    background: linear-gradient(135deg, #a900ff, #6814dc, #a300ff);
    border: 5px solid #7900c9;
    border-radius: 35px;
    transform: rotate(-5deg);
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-size: clamp(75px, 15vw, 115px);
    font-weight: 900;
    text-shadow: 2px 5px 5px #451080;
    box-shadow: 0 8px 15px rgba(0,0,0,.3);
}

.ticket::before,
.ticket::after {
    content: "";
    position: absolute;
    width: 42px;
    height: 42px;
    background: #777;
    border-radius: 50%;
    top: 50%;
    transform: translateY(-50%);
}

.ticket::before {
    left: -23px;
}

.ticket::after {
    right: -23px;
}

/* 하단 버튼 영역 */
.coupon-box {
    position: relative;
    background: white;
    padding: 25px;
    border-radius: 15px;
    margin-top: -5px;
}

.coupon-button {
    width: 100%;
    padding: 27px 10px;
    border: none;
    border-radius: 12px;
    background: black;
    color: white;
    font-size: 25px;
    font-weight: bold;
    cursor: pointer;
}

.coupon-button:active {
    transform: scale(.98);
}

.notice {
    color: #aaa;
    font-size: 14px;
    line-height: 1.7;
    margin-top: 20px;
}

/* 쿠폰 발급 완료 */
.success {
    display: none;
    background: white;
    padding: 35px 20px;
    border-radius: 15px;
}

.success h2 {
    color: #5d28c5;
    margin-bottom: 15px;
}

.success p {
    color: #777;
    line-height: 1.7;
}

/* 하단 배너 */
.bottom-banner {
    position: fixed;
    bottom: 25px;
    left: 3%;
    width: 94%;
    background: #07151a;
    color: white;
    padding: 22px;
    border: 2px solid #126d67;
    border-radius: 20px;
    font-weight: bold;
    text-align: center;
    z-index: 2;
}

@media(max-width: 480px) {
    .orange {
        min-height: 400px;
        padding-top: 95px;
    }

    .ticket {
        height: 125px;
    }

    .coupon-box {
        padding: 18px;
    }

    .coupon-button {
        font-size: 22px;
        padding: 23px 5px;
    }
}
</style>
</head>

<body>

<!-- 메인 쇼핑 페이지 -->
<header class="header">
    우리집 🛎
</header>

<div class="search">
    음식 검색하기 🔍
</div>

<div class="banner">
    배달 할인 이벤트 🎉
    <br>
    오늘만 특별한 혜택!
</div>

<div class="categories">
    <div class="category"><span>🍗</span>치킨</div>
    <div class="category"><span>🍕</span>피자</div>
    <div class="category"><span>🍜</span>중식</div>
    <div class="category"><span>🍣</span>일식</div>
    <div class="category"><span>🍖</span>고기</div>
    <div class="category"><span>🥗</span>샐러드</div>
    <div class="category"><span>🍔</span>햄버거</div>
    <div class="category"><span>☕</span>카페</div>
</div>

<section class="foods">
    <h2>인기 메뉴</h2>
    <br>
    <div class="food-grid">
        <div class="food">
            <div class="food-image">🍗</div>
            <p>바삭한 치킨</p>
            <small>20,000원</small>
        </div>
        <div class="food">
            <div class="food-image">🍕</div>
            <p>치즈 피자</p>
            <small>18,000원</small>
        </div>
        <div class="food">
            <div class="food-image">🍜</div>
            <p>매콤한 짬뽕</p>
            <small>12,000원</small>
        </div>
        <div class="food">
            <div class="food-image">🍔</div>
            <p>수제 버거</p>
            <small>10,000원</small>
        </div>
    </div>
</section>

<div class="bottom-banner" id="bottomBanner">
    ✨ 배달페이 최대 5% 포인트 적립
    <span onclick="this.parentElement.style.display='none'"
    style="float:right;cursor:pointer;">✕</span>
</div>

<!-- 할인 팝업 -->
<div class="overlay" id="overlay">

    <div class="popup">

        <button class="close" onclick="closePopup()">×</button>

        <div id="promotion">

            <div class="orange">
                <h2>오늘 할인!</h2>
                <div class="amount">6,000원</div>
                <div class="sale">할인</div>
            </div>

            <div class="ticket">%</div>

            <div class="coupon-box">

                <button class="coupon-button"
                onclick="getCoupon()">
                    지금 쿠폰 받기 ❯
                </button>

                <p class="notice">
                    특정 브랜드 한정 프로모션으로,
                    수량 소진 시 조기 종료될 수 있습니다.
                    <br>
                    최소 주문금액은 21,000원입니다.
                </p>

            </div>

        </div>

        <div class="success" id="success">

            <h2>🎉 쿠폰 발급 완료!</h2>

            <p>
                6,000원 할인 쿠폰이 발급되었습니다.
                <br>
                주문 시 쿠폰을 적용해 주세요.
            </p>

            <button class="coupon-button"
            onclick="closePopup()">
                쇼핑 계속하기
            </button>

        </div>

    </div>
</div>

<script>

// 팝업 닫기
function closePopup() {
    document.getElementById("overlay").style.display = "none";
}

// 쿠폰 받기
function getCoupon() {

    document.getElementById("promotion").style.display = "none";

    document.getElementById("success").style.display = "block";

}

// 배경 클릭 시 팝업 닫기
document.getElementById("overlay").addEventListener("click", function(e) {
    if(e.target === this) {
        closePopup();
    }
});

</script>

</body>
</html>
