<script>
let sections = document.querySelectorAll('section');
let navLinks = document.querySelectorAll('header nav a');

window.onscroll = () => {
    sections.forEach(sec => {
        let top = window.scrollY;
        let offset = sec.offsetTop - 150;
        let height = sec.offsetHeight;
        let id = sec.getAttribute('id');

        if(top >= offset && top < offset + height) {
            navLinks.forEach(links => {
                links.classList.remove('active');
                document.querySelector('header nav a[href*=' + id +']').classList.add('active');
            });
        };
    });
};
</script>
<template>
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
 <!--navbar-->
 <header class="header">
        <a href="#" class="logo">Ibnu.</a>
            <nav>
                <a href="#home" style='--i:1;' class="active">Home</a>
                <a href="#about" style='--i:2;' >About</a>
                <a href="#service" style='--i:3;' >Services</a>
                <a href="#project" style='--i:4;' >Project</a>
                <a href="#contact" style='--i:5;' >Contact</a>
            </nav>
        </header> 

    <!--Home Content-->
        <section id="home">
            <div class="home-content">
            <h1>Hi, I'm Syaifuddin</h1>
            <h3>Web Developer</h3>
            <p>Halo, saya Syafuddin Ibnu Romadhon, seorang web developer berpengalaman yang memiliki passion tinggi dalam menciptakan pengalaman pengguna yang luar biasa melalui desain web yang inovatif dan fungsional. Saya memiliki keahlian dalam mengembangkan situs web responsif, aplikasi web dinamis, dan solusi e-commerce yang efisien.</p>
                <div class="btn-box">
                    <a href="#">Download CV</a>
                </div>
        </div>
        <div class="home-sci">
            <a href="" style="--i:1"><i class='bx bxl-facebook'></i></a>
            <a href="https://www.instagram.com/syfdn002/" style="--i:2"><i class='bx bxl-instagram' ></i></a>
            <a href="https://www.youtube.com/channel/UC43Ee8fc4e-uJoNveOIYKPg" style="--i:3"><i class='bx bxl-youtube'></i></a>
            <a href="" style="--i:4"><i class='bx bxl-linkedin'></i></a> 
        </div>
        <div class="profil">
            <img src="./assets/profil.png" alt="">
        </div>
    </section>

    <!--About Content-->
    <section id="about">
        <h2 class="heading">About <span>Me</span></h2>
        <div class="about-img">
            <img src="./assets/FotoProfil.png" alt="">
            <span class="circle-spin"></span>
        </div>
        <div class="about-content">
            <h3>Web Developer</h3>
            <p>Halo, saya Syafuddin Ibnu Romadhon, Berpendidikan di Universitas Islam Riau,Saya seorang web developer yang baru saja belajar , ajarin dong puh sepuh </p>
        </div>
        <div class="btn-box btns">
            <a href="" class="btn">Read More</a>
        </div>
    </section>

    <!--Service Content-->
    <section id="service">
        <div class="center-text">
            <h2>My <span>Service</span></h2>
        </div>
        <div class="service-content">
            <div class="box">
                <img src="./assets/image/design.png" alt="">
                <h3>UI/UX Design</h3>
                <p>Terampil dalam membuat ui/ux design tapi masih belajar</p>
                <a href="#">
                    Lihat Selengkapnya
                    <i class='bx bx-right-arrow-alt'></i>
                </a>
            </div>

            <div class="box">
                <img src="./assets/image/web.png" alt="" class="">
                <h3>Frontend</h3>
                <p>Mahir dalam pembuatan web statis masih sikit</p>
                <a href="#">
                    Lihat Selengkapnya
                    <i class='bx bx-right-arrow-alt'></i>
                </a>
            </div>

            <div class="box">
                <img src="./assets/image/data.png" alt="" class="">
                <h3>Data science</h3>
                <p>Memiliki kemampuan di database tapi masih sikit</p>
                <a href="#">
                    Lihat Selengkapnya
                    <i class='bx bx-right-arrow-alt'></i>
                </a>
            </div>
        </div>
    </section>
    <!--Content Project-->
    <section id="project">
        <div class="center-text">
            <h2> My <span>Project</span></h2>
        <div class="project-content">
            <div class="row">
                <img src="./assets/image/project.png" alt="">
                    <div class="row-text">
                        <h5>Web Portofolio</h5>
                    </div>
                    <div class="row-icon">
                        <i class='bx bxl-github' ></i>
                    </div>
                        <h4>Its my web portofolio</h4>
            </div>
        </div>
    </div>
    </section>
    <!--Contact Conten-->
    <section id="contact">
        <div class="center-text">
            <h2>Contact <span>Me</span></h2>
        </div>

        <div class="contact-form">
            <form action="">
                <input type="text" placeholder="Masukkan nama..." required>
                <input type="email" placeholder="Alamat Email..." required>
                <textarea name="" id="" cols="30" rows="10" placeholder="Tambahkan pesan disini..." required></textarea>
                <input type="Submit" name="" id="" value="Kirimkan Pesan" class="send-btn">
            </form>
        </div>

        <div class="footer">
            <div class="copyright">
                <p>2023 @S.Ibnu Romadhon, All right Reserved</p>
            </div>

            <a href="#home" class="scroll-top">
                <i class='bx bxs-up-arrow-circle'></i>
            </a>
        </div>
    </section>
</template> 

<style>
@import url('https://fonts.googleapis.com/css?family=Poppins:400,700,900');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
    scroll-behavior: smooth;
}

body{
    background: #081b29;
    color: #ededed;
}

.header{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px 10%;
    background: rgba(255, 255, 255, .1);
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 100;
    backdrop-filter: blur(10px);
    box-shadow: 5px rgba(255, 255, 255, .1);

}

.logo{
    font-size: 20px;
    color: #ededed;
    text-decoration: none;
    font-weight: 600;
    opacity: 0;
    animation: slideRight 1s ease forwards;
}

nav a {
    font-size: 17px;
    color: #ededed;
    text-decoration: none;
    font-weight: 500;
    margin-left: 35px;
    transition: .3s;
    opacity: 0;
    animation: slideTop .5s ease forwards;
    animation-delay: calc(.2s* var(--i));
}

nav a:hover,
nav a.active {
    color: rgb(127, 232, 255);
}

/*Bagian Home*/

#home {
    height: 100vh;
    display: flex;
    align-items: center;
    padding: 0 10%;
}

.profil img{
    position: relative;
    max-width: 80%;
    height: auto;
    opacity: 0;
    animation: slideLeft 2s ease forwards;
}

.home-content {
    max-width: 600px;
}

.home-content h1{
    font-size: 55px;
    font-display: 20px;
    opacity: 0;
    animation: slideBottom 1s ease forwards;
    animation-delay: .2s;
}

.home-content h3 {
    font-size: 40px;
    font-weight: 600;
    color: rgb(127, 232, 255);
    animation: slideRight 1s ease forwards;
}

.home-content p {
    font-size: 16px;
    font-weight: 500;
    margin: 20px 0 50px;
    opacity: 0;
    animation: slideLeft 1s ease forwards;
}

.home-content .btn-box {
    display: flex;
    justify-content: space-between;
    width: 450px;
    height: 40px;
    background: transparent;
}

.btn-box a {
    position: relative;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 180px;
    height: 100%;
    background: rgb(127, 232, 255);
    border-radius: 20px;
    font-size: 15px;
    color: #081b29;
    text-decoration: none;
    font-weight: 600;
    letter-spacing: 1px;
    transition: .5s;
    opacity: 0;
    animation: slideTop 1s ease forwards;
}

.btn-box a:hover {
    color: #081b29;
    background: rgb(127, 232, 255);
    box-shadow: 0 0 10px rgb(127, 232, 255), 0 0 20px rgb(127, 232, 255), 0 0 30px rgb(127, 232, 255);
}

.home-sci  {
    position: absolute;
    bottom: 4rem;
    width: 210px;
    display: flex;
    justify-content: space-between;
}

.home-sci a {
    position: relative;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    background: transparent;
    border: .2rem solid rgb(127, 232, 255);
    border-radius: 50%;
    font-size: 20px;
    color:rgb(127, 232, 255);
    z-index: 1;
    overflow: hidden;
    text-decoration: none;
    transition: .5s;
    animation: slideTop .5s ease forwards;
    animation-delay: calc(.1s* var(--i));
}

.home-sci a:hover {
    color: #081b29;
    background: rgb(127, 232, 255);
    box-shadow: 0 0 10px rgb(127, 232, 255), 0 0 20px rgb(127, 232, 255), 0 0 30px rgb(127, 232, 255);
}
/*Bagian About*/

#about {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    gap: 2rem;
    height: 100vh;
    padding-bottom: 6rem;
    padding: 0 10%;
    background: #142c51;

}
.about-content h2 {
    display: flex;
    justify-content: center; 
    align-items: center;
    height: 50px; 
    margin: 0;
    font-size: 35px;
}

.about-img {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 15rem;
    height: 15rem;
    
}

.about-img img{
    width: 100%;

}

.about-img .circle-spin {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%)rotate(0);
    width: 110%;
    height: 110%;
}

.heading {
    font-size: 4rem;
    margin-bottom: 3rem;
    text-align: center;
}

.about-content {
    text-align: center
}

.about-content h3 {
    font-size: 2.6rem;
}

span{
    color: rgb(127, 232, 255);
}


#service {
    min-height: 100vh;
    justify-content: center;
    padding: 0 10%;
    background: #081b29;
}

.center-text {
    text-align: center;
}

.center-text h2 {  
    margin-top: 100px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    height: 200px; 
    margin: 0;
    font-size: 60px;;
}
.center-text span {
    margin-left: 10px;
}

.service-content{
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, auto));
    align-items: center;
    gap: 2.3rem;
    margin-top: 4.2rem;
}

.box {
    padding: 45px 40px 66px;
    background: hsl(216, 60%, 20%);
    border-radius: 28px;
    box-shadow: 0 0 5px rgb(127, 232, 255);
    transition: all .50s ease;
    cursor: pointer;

}

.box img {
    margin-bottom: 20px;
}

.box h3{
    font-size: 30px;
    font-weight: 700;
    margin-bottom: 10px;
}

.box p{
    font-size: 15px;
    font-weight: 400;
    color: #ededed;
    line-height: 30px;
    margin-bottom: 20px;
}

.box a {
    display: inline-block;
    font-size: 22px;
    line-height: 1.273em;
    font-weight: 700;
    padding: 7px 0;
    color: rgb(127, 232, 255);
    border-bottom:  2px white;
    transition: all .50s ease;
    text-decoration: none;

}

.box a:hover {
    border-bottom: rgb(127, 232, 255);
}

.box i {
    vertical-align: middle;
    font-size: 25px;
    color: rgb(127, 232, 255);
    margin-left: 5px;
}

.box:hover {
    border: 1px solid rgb(127, 232, 255);
    transform: translateY(-5px) scale(1.03);
}

#project {
    height: 100vh;
    padding: 0 10%;
    background: #142c51;
}

.project-content{
    display: flex;
    grid-template-columns: repeat(auto-fit, minmax(300px, auto));
    align-items: center;
    gap: 2.3rem;
    margin-top: 4.2rem;
}

.row img{
    height: auto;
    width: 100%;
    border-radius: 28px;
    max-width: 330px;
}

.row {
    background: #142c51;
    border-radius: 28px;
    border: 1px solid transparent;
    padding: 20px;
    box-shadow: 0 0 5px rgb(127, 232, 255);
    transition: all .50s ease;
}

.row h5{
    font: 20px;
    font-weight: 600;
    color: #ededed;
}

.row i {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 55px;
    height: 55px;
    font-size: 27px;
    border-radius: 50%;
    color: #142c51;
    background: rgb(127, 232, 255);
}
.row h5{
    font: 20px;
    font-weight: 700;
    margin-bottom: 10px;
    line-height: 1.4;
}

#contact {
    height: 100vh;
    padding: 0 10%;
    background: #081b29;
}

.contact-form {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 4.2rem;
}

.contact-form form {
    position: relative;
    width: 600px;
}

form input,
form textarea{
    background: fixed;
    width: 100%;
    padding: 10px;
    border: none;
    outline: none;
    box-shadow: 0 0 5px rgb(127, 232, 255);
    margin-bottom: 15px;
    border-radius: 8px;
    color: #ededed;
}

form input::placeholder,
form textarea::placeholder {
    color: #ededed;
    font-size: 15px;
}

form .send-btn{
    position: relative;
    display: inline-flex;
    justify-content: center;
    width: 150px;
    height: 20%;
    font-size: 15px;
    color: #ededed;
    text-decoration: none;
    font-weight: 600;
    letter-spacing: 1px;
    transition: .5s;
    opacity: 0;
    animation: slideTop 1s ease forwards;
}

form .send-btn:hover {
    color: #081b29;
    background: rgb(127, 232, 255);
    box-shadow: 0 0 10px rgb(127, 232, 255), 0 0 20px rgb(127, 232, 255), 0 0 30px rgb(127, 232, 255);
}

.footer {
    padding: 22px;
    background: #081b29;
    align-items: center;
    display: flex;
    justify-content: space-between;
    gap: 2rem;
}

.scroll-top i {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 45px;
    height: 45px;
    border-radius: 50%;
    color: rgb(127, 232, 255);
    font-size: 25px;
}

/*KEYFRAME ANIMATION*/
@keyframes slideRight {0%{
    transform: translateX(-100px);
    opacity: 0;
    }
    100%{
        transform: translateX(0);
        opacity: 1;
    }
}

@keyframes slideTop { 0% {
    transform: translateY(100px);
    opacity: 0;
    }
    100%{
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes slideBottom { 0% {
    transform: translateY(-100px);
    opacity: 0;
    }
    100%{
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes slideLeft { 0% {
    transform: translateX(100px);
    opacity: 0;
    }
    100%{
        transform: translateX(0);
        opacity: 1;
    }
}

@media (max-width: 1700px){
    header {
        padding: 20px 8%;
    }
    header.sticky{
        padding: 14px 8% 80%;
    }
    section{
        padding: 90px 8% 80px;
    }
    .footer{
        padding: 18px 8%;
    }
    .logo{
        font-size: 28px;
    }
}
</style>