
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>오늘의 3,000원 할인</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:Arial,sans-serif;background:#f5f5f5;padding-bottom:80px}
header{background:white;padding:22px;font-size:24px;font-weight:bold}
.search{margin:15px;padding:15px;border:1px solid #ddd;border-radius:30px;background:white;color:#888}
.banner{margin:15px;padding:30px;background:#e9e5ff;color:#5030a5;font-size:24px;font-weight:bold;border-radius:15px}
.categories{display:grid;grid-template-columns:repeat(4,1fr);gap:20px;padding:25px 10px;background:white;text-align:center}
.categories span{display:block;font-size:30px;margin-bottom:8px}
.foods{padding:20px}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.food{background:white;padding:12px;border-radius:12px}
.food-image{height:100px;background:#ffe6ca;border-radius:10px;display:grid;place-items:center;font-size:50px}
.food p{margin-top:10px;font-weight:bold}

.overlay{position:fixed;inset:0;background:rgba(0,0,0,.65);display:flex;align-items:center;justify-content:center;padding:15px;z-index:10}
.popup{width:100%;max-width:490px;position:relative;text-align:center}
.close{position:absolute;right:0;top:-48px;width:45px;height:45px;border:0;border-radius:50%;background:white;font-size:30px;cursor:pointer}

.orange{width:88%;margin:auto;min-height:360px;padding:90px 10px 65px;background:#ff4b0b;color:white;clip-path:polygon(13% 0,100% 0,88% 58%,100% 58%,83% 100%,0 83%);transform:rotate(-3deg)}
.orange h1{font-size:clamp(32px,8vw,52px);color:#511900;font-style:italic;font-weight:900}
.amount{font-size:clamp(55px,13vw,83px);font-weight:900;font-style:italic;white-space:nowrap;margin:10px 0}
.sale{font-size:48px;font-weight:900;color:#5a1b00;text-align:right;padding-right:20px}

.ticket{width:75%;height:120px;margin:-15px auto 0;background:linear-gradient(135deg,#a900ff,#6814dc,#a300ff);border:5px solid #7900c9;border-radius:28px;transform:rotate(-5deg);display:grid;place-items:center;color:white;font-size:100px;font-weight:900;text-shadow:2px 5px 5px #451080;box-shadow:0 8px 15px #0005;position:relative}
.ticket:before,.ticket:after{content:"";position:absolute;width:36px;height:36px;border-radius:50%;background:#777;top:50%;transform:translateY(-50%)}
.ticket:before{left:-22px}
.ticket:after{right:-22px}

.coupon-box{background:white;padding:18px;border-radius:14px;margin-top:-3px}
.get-button{width:100%;padding:23px 5px;background:black;color:white;border:0;border-radius:11px;font-size:23px;font-weight:bold;cursor:pointer}
.notice{font-size:13px;color:#aaa;line-height:1.7;margin-top:15px}
.success{display:none;background:white;padding:35px 20px;border-radius:14px}
.success h2{color:#6425c9}
.success p{margin:15px 0;color:#777;line-height:1.7}
.bottom{position:fixed;bottom:14px;left:3%;width:94%;padding:17px;background:#07151a;color:white;border:2px solid #126d67;border-radius:16px;text-align:center;font-weight:bold;z-index:2}

@media(max-width:360px){
.orange{min-height:310px;padding-top:75px}
.ticket{height:100px;font-size:80px}
.get-button{font-size:19px}
}
</style>
</head>

<body>

<header>우리집 🛎</header>

<div class="search">음식 검색하기 🔍</div>

<div class="banner">
배달 할인 이벤트 🎉<br>
오늘만 특별한 혜택!
</div>

<div class="categories">
<div><span>🍗</span>치킨</div>
<div><span>🍕</span>피자</div>
<div><span>🍜</span>중식</div>
<div><span>🍣</span>일식</div>
<div><span>🍖</span>고기</div>
<div><span>🥗</span>샐러드</div>
<div><span>🍔</span>햄버거</div>
<div><span>☕</span>카페</div>
</div>

<section class="foods">
<h2>인기 메뉴</h2><br>
<div class="grid">
<div class="food">
<div class="food-image">🍗</div>
<p>바삭한 치킨</p>20,000원
</div>
<div class="food">
<div class="food-image">🍕</div>
<p>치즈 피자</p>18,000원
</div>
<div class="food">
<div class="food-image">🍜</div>
<p>매콤한 짬뽕</p>12,000원
</div>
<div class="food">
<div class="food-image">🍔</div>
<p>수제 버거</p>10,000원
</div>
</div>
</section>

<div class="bottom">✦ 배달페이 최대 5% 포인트 적립</div>

<!-- 할인 팝업 -->
<div class="overlay" id="overlay">
<div class="popup">

<button class="close" onclick="closePopup()">×</button>

<div id="promotion">

<div class="orange">
<h1>오늘 할인!</h1>
<div class="amount">3,000원</div>
<div class="sale">할인</div>
</div>

<div class="ticket">%</div>

<div class="coupon-box">
<button class="get-button" onclick="getCoupon()">
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

<!-- 쿠폰 발급 성공 -->
<div class="success" id="success">
<h2>🎉 쿠폰 발급 완료!</h2>
<p>
3,000원 할인 쿠폰이 발급되었습니다.
<br>
주문 시 쿠폰을 적용해 주세요.
</p>
<button class="get-button" onclick="closePopup()">
쇼핑 계속하기
</button>
</div>

</div>
</div>

<script>
function closePopup(){
document.getElementById("overlay").style.display="none";
}

function getCoupon(){
document.getElementById("promotion").style.display="none";
document.getElementById("success").style.display="block";
}

document.getElementById("overlay").addEventListener("click",function(e){
if(e.target===this) closePopup();
});

document.addEventListener("keydown",function(e){
if(e.key==="Escape") closePopup();
});
</script>

</body>
</html>
