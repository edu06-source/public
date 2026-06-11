[자기소개 웹페이지.html](https://github.com/user-attachments/files/28824373/default.html)
# public<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>윤상원 | Portfolio</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Montserrat:wght@600;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

<style>
:root{
    --bg:#0f172a;
    --surface:#1e293b;
    --surface-2:rgba(30,41,59,.65);
    --accent:#14b8a6;
    --accent-light:#38bdf8;
    --text:#e2e8f0;
    --muted:#94a3b8;
    --border:rgba(255,255,255,.08);
    --shadow:0 10px 30px rgba(0,0,0,.3);
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:'Inter',sans-serif;
    background:var(--bg);
    color:var(--text);
    line-height:1.7;
    overflow-x:hidden;
}

body::before{
    content:"";
    position:fixed;
    inset:0;
    background:
        radial-gradient(circle at 20% 20%, rgba(20,184,166,.12), transparent 25%),
        radial-gradient(circle at 80% 30%, rgba(56,189,248,.12), transparent 25%),
        radial-gradient(circle at 50% 80%, rgba(20,184,166,.08), transparent 30%);
    pointer-events:none;
    z-index:-2;
}

a{
    text-decoration:none;
    color:inherit;
}

img{
    max-width:100%;
}

.container{
    width:min(1150px,92%);
    margin:auto;
}

section{
    padding:90px 0;
}

.section-title{
    text-align:center;
    margin-bottom:50px;
}

.section-title h2{
    font-family:'Montserrat',sans-serif;
    font-size:clamp(2rem,5vw,3rem);
    margin-bottom:12px;
}

.section-title p{
    color:var(--muted);
}

/* NAV */

header{
    position:fixed;
    width:100%;
    top:0;
    z-index:1000;
    backdrop-filter:blur(14px);
    background:rgba(15,23,42,.8);
    border-bottom:1px solid rgba(255,255,255,.05);
}

.navbar{
    height:75px;
    display:flex;
    justify-content:space-between;
    align-items:center;
}

.logo{
    font-family:'Montserrat',sans-serif;
    font-weight:800;
    font-size:1.3rem;
    letter-spacing:1px;
}

.logo span{
    color:var(--accent);
}

.nav-links{
    display:flex;
    gap:30px;
    list-style:none;
}

.nav-links a{
    color:var(--muted);
    transition:.3s;
}

.nav-links a:hover{
    color:var(--accent);
}

.menu-btn{
    display:none;
    width:48px;
    height:48px;
    border:none;
    background:none;
    color:var(--text);
    font-size:1.4rem;
    cursor:pointer;
}

/* HERO */

.hero{
    min-height:100vh;
    display:flex;
    align-items:center;
    position:relative;
    overflow:hidden;
}

.hero::before{
    content:"";
    position:absolute;
    inset:0;
    background:
    linear-gradient(135deg, rgba(20,184,166,.12), transparent 45%),
    linear-gradient(-135deg, rgba(56,189,248,.12), transparent 45%);
}

.hero-grid{
    display:grid;
    gap:40px;
}

.hero-content{
    text-align:center;
}

.badge{
    display:inline-flex;
    align-items:center;
    gap:8px;
    padding:10px 18px;
    border-radius:999px;
    background:rgba(20,184,166,.12);
    border:1px solid rgba(20,184,166,.25);
    color:var(--accent);
    margin-bottom:20px;
}

.hero h1{
    font-family:'Montserrat',sans-serif;
    font-size:clamp(2.8rem,8vw,5rem);
    line-height:1.1;
    margin-bottom:18px;
}

.hero h1 span{
    color:var(--accent);
}

.hero p{
    max-width:700px;
    margin:auto;
    color:var(--muted);
    font-size:1.1rem;
}

.hero-buttons{
    margin-top:35px;
    display:flex;
    gap:16px;
    justify-content:center;
    flex-wrap:wrap;
}

.btn{
    min-height:48px;
    padding:14px 24px;
    border-radius:14px;
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:10px;
    font-weight:600;
    transition:.35s;
    cursor:pointer;
}

.btn-primary{
    background:linear-gradient(135deg,var(--accent),var(--accent-light));
    color:#fff;
}

.btn-secondary{
    background:rgba(255,255,255,.05);
    border:1px solid var(--border);
}

.btn:hover{
    transform:translateY(-4px);
}

/* CARDS */

.grid{
    display:grid;
    gap:24px;
}

.card{
    background:var(--surface-2);
    border:1px solid var(--border);
    backdrop-filter:blur(14px);
    border-radius:24px;
    padding:28px;
    box-shadow:var(--shadow);
    transition:.35s;
}

.card:hover{
    transform:translateY(-8px);
    border-color:rgba(20,184,166,.3);
}

.info-grid{
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
}

.info-item{
    text-align:center;
}

.info-item i{
    color:var(--accent);
    font-size:1.8rem;
    margin-bottom:14px;
}

.info-item h3{
    margin-bottom:8px;
}

/* ABOUT */

.about-content{
    text-align:center;
    max-width:850px;
    margin:auto;
}

.about-content p{
    color:var(--muted);
}

/* HOBBIES */

.hobby-grid{
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
}

.hobby-card{
    text-align:center;
}

.hobby-card i{
    font-size:2.3rem;
    color:var(--accent);
    margin-bottom:15px;
}

/* CONTACT */

.contact-card{
    max-width:700px;
    margin:auto;
    text-align:center;
}

.contact-email{
    display:inline-flex;
    align-items:center;
    gap:12px;
    margin-top:20px;
    padding:14px 22px;
    border-radius:16px;
    background:rgba(20,184,166,.1);
    color:var(--accent);
    word-break:break-all;
}

/* FOOTER */

footer{
    padding:30px 0;
    text-align:center;
    color:var(--muted);
    border-top:1px solid rgba(255,255,255,.05);
}

/* ANIMATION */

.fade{
    opacity:0;
    transform:translateY(40px);
    transition:all .8s ease;
}

.fade.show{
    opacity:1;
    transform:translateY(0);
}

/* MOBILE */

@media (max-width:767px){

    .nav-links{
        position:absolute;
        top:75px;
        left:0;
        width:100%;
        background:rgba(15,23,42,.98);
        flex-direction:column;
        text-align:center;
        padding:25px 0;
        display:none;
        border-bottom:1px solid rgba(255,255,255,.05);
    }

    .nav-links.active{
        display:flex;
    }

    .menu-btn{
        display:block;
    }
}

@media (min-width:768px){
    .hero-grid{
        grid-template-columns:1fr;
    }
}

@media (min-width:1024px){
    .hero-content{
        text-align:center;
    }
}
</style>
</head>

<body>

<header>
    <div class="container navbar">
        <div class="logo">YOON<span>.</span></div>

        <nav aria-label="주요 메뉴">
            <ul class="nav-links" id="navLinks">
                <li><a href="#home">홈</a></li>
                <li><a href="#about">소개</a></li>
                <li><a href="#profile">프로필</a></li>
                <li><a href="#hobbies">취미</a></li>
                <li><a href="#contact">연락처</a></li>
            </ul>
        </nav>

        <button class="menu-btn" id="menuBtn" aria-label="메뉴 열기">
            <i class="fas fa-bars"></i>
        </button>
    </div>
</header>

<main>

<section class="hero" id="home">
    <div class="container hero-grid">
        <div class="hero-content fade">
            <div class="badge">
                <i class="fas fa-star"></i>
                PERSONAL PORTFOLIO
            </div>

            <h1>안녕하세요.<br><span>윤상원</span>입니다.</h1>

            <p>
                사람과의 관계를 중요하게 생각하며 긍정적인 에너지와 책임감을 바탕으로
                성장해 나가는 ESFJ입니다. 새로운 경험을 즐기고 다양한 사람들과 함께
                배우며 발전하는 것을 좋아합니다.
            </p>

            <div class="hero-buttons">
                <a href="#about" class="btn btn-primary">
                    <i class="fas fa-user"></i>
                    더 알아보기
                </a>

                <a href="#contact" class="btn btn-secondary">
                    <i class="fas fa-envelope"></i>
                    연락하기
                </a>
            </div>
        </div>
    </div>
</section>

<section id="about">
    <div class="container">
        <div class="section-title fade">
            <h2>About Me</h2>
            <p>나를 소개합니다</p>
        </div>

        <div class="card about-content fade">
            <p>
                저는 사람들과의 소통을 즐기며 협력 속에서 더 큰 가치를 만들어내는 것을 중요하게 생각합니다.
                긍정적인 태도와 배려심을 바탕으로 주변 사람들과 좋은 관계를 형성하고,
                새로운 도전과 경험을 통해 꾸준히 성장하고자 합니다.
                좋아하는 것은 싫어하는 것을 제외한 거의 모든 것이며,
                열린 마음으로 다양한 분야를 경험하는 것을 즐깁니다.
            </p>
        </div>
    </div>
</section>

<section id="profile">
    <div class="container">
        <div class="section-title fade">
            <h2>Profile</h2>
            <p>기본 정보</p>
        </div>

        <div class="grid info-grid">
            <div class="card info-item fade">
                <i class="fas fa-user"></i>
                <h3>이름</h3>
                <p>윤상원</p>
            </div>

            <div class="card info-item fade">
                <i class="fas fa-brain"></i>
                <h3>MBTI</h3>
                <p>ESFJ</p>
            </div>

            <div class="card info-item fade">
                <i class="fas fa-droplet"></i>
                <h3>혈액형</h3>
                <p>AB형</p>
            </div>

            <div class="card info-item fade">
                <i class="fas fa-heart"></i>
                <h3>좋아하는 것</h3>
                <p>싫어하는 것을 제외한 모든 것</p>
            </div>
        </div>
    </div>
</section>

<section id="hobbies">
    <div class="container">
        <div class="section-title fade">
            <h2>Hobbies</h2>
            <p>취미와 관심사</p>
        </div>

        <div class="grid hobby-grid">
            <div class="card hobby-card fade">
                <i class="fas fa-baseball"></i>
                <h3>야구</h3>
                <p>
                    팀워크와 전략이 어우러지는 스포츠를 좋아하며
                    경기 관람과 관련 이야기를 즐깁니다.
                </p>
            </div>

            <div class="card hobby-card fade">
                <i class="fas fa-person-running"></i>
                <h3>러닝</h3>
                <p>
                    꾸준한 운동을 통해 체력과 집중력을 관리하며
                    건강한 라이프스타일을 추구합니다.
                </p>
            </div>

            <div class="card hobby-card fade">
                <i class="fas fa-beer-mug-empty"></i>
                <h3>음주</h3>
                <p>
                    좋은 사람들과 함께하는 시간을 소중하게 여기며
                    즐거운 대화와 교류를 좋아합니다.
                </p>
            </div>
        </div>
    </div>
</section>

<section id="contact">
    <div class="container">
        <div class="section-title fade">
            <h2>Contact</h2>
            <p>언제든지 연락주세요</p>
        </div>

        <div class="card contact-card fade">
            <h3 style="margin-bottom:15px;">함께 성장하고 소통하는 것을 좋아합니다.</h3>
            <p style="color:var(--muted);">
                새로운 인연과 다양한 기회를 환영합니다.
            </p>

            <a href="mailto:cfp6363@naver.com" class="contact-email" aria-label="이메일 보내기">
                <i class="fas fa-envelope"></i>
                cfp6363@naver.com
            </a>
        </div>
    </div>
</section>

</main>

<footer>
    <div class="container">
        © 2026 윤상원 Portfolio. All Rights Reserved.
    </div>
</footer>

<script>
const menuBtn = document.getElementById('menuBtn');
const navLinks = document.getElementById('navLinks');

menuBtn.addEventListener('click', () => {
    navLinks.classList.toggle('active');
});

document.querySelectorAll('.nav-links a').forEach(link=>{
    link.addEventListener('click',()=>{
        navLinks.classList.remove('active');
    });
});

const observer = new IntersectionObserver((entries)=>{
    entries.forEach(entry=>{
        if(entry.isIntersecting){
            entry.target.classList.add('show');
        }
    });
},{
    threshold:0.15
});

document.querySelectorAll('.fade').forEach(el=>{
    observer.observe(el);
});
</script>

</body>
</html>
