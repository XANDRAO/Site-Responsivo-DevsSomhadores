# Site-Responsivo-DevsSomhadores
<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">"
    <link rel="stylesheet" href="estilo.css">
    <title>Document</title>
</head>
<body>
     <div class="container">
          <nav>
               <div class="logo">
                    <a href="inde.html">DEVS SONHADORES</a>
               </div>
               <ul>
                    <li> <a href="#">Pagina Inicial</a></li>
                    <li> <a href="#">Serviços</a></li>
                    <li> <a href="#">Team</a></li>
                    <li> <a href="#">Blog</a></li>
                    <li> <a href="#">Fale conosco</a></li>
                    <li> <a href="#">Entrar</a></li>
                    <button>Cadastre-se</button>
               </ul>
                <div class="menu-icon">
                    <img src="imagens/menu.png">
                </div>
          </nav>
          <main>
            <div class="text-bx">
                <h1> Cresça o seu negócio com <b> marketing digital</b></h1>
                <p>
                    Tudo que você precisa saber esta aqui se cadastre 
                    no nosso site para saber mais, se quiser conhecer mais a nossa empresa
                    estamos em todas as redes sociais! 
                </p>
                <div class="input-bx">
                    <input type="email" placeholder="Endereço de email">
                    <button>Ver mais</button>
                </div>
                <div class="midias-sociais">
                    <a href="#"><i class="fa fa-instagram"></i></a>
                    <a href="#"><i class="fa fa-facebook"></i></a>
                    <a href="#"><i class="fa fa-twitter"></i></a>
                    <a href="#"><i class="fa fa-youtube"></i></a>
                    <a href="#"><i class="fa fa-whatsapp"></i></a>
                </div>
                
            </div>

            <div class="img-bx">
                <img src="imagens/jornada-marketing.png">
            </div>
          </main>
     </div>

     <script src="main.js"></script>
</body>
</html>

@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,900&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
body{
    background-color: #e3f0ff;
    min-height: 100vh;
}
.container{
    max-width: 1300px;
    margin: 0 auto;
    padding: 0 4%;
}
nav{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 100px;

}
nav .menu-icon{
    cursor: pointer;
    display: none;
}
nav .logo a{
    font-size: 30px;
    font-weight: bold;
    color: #5654b3;
    text-decoration: none;
}
nav ul{
    display: flex;
    list-style: none;
    align-items: center;
}
nav ul li{
    padding: 0 15px;
}
nav ul li a{
    text-decoration: none;
    font-size: 17px;
    text-transform: uppercase;
    color: #5654b3;
}
nav ul button{
    border: none;
    background-color: #5654b3;
    color: white;
    padding: 10px 20px;
    border-radius: 5px;
    font-size: 16px;
    letter-spacing: 1px;
    margin-left: 20px;
    cursor: pointer;
}
main{
    margin-top: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;

}
.text-bx{
    width: 40%;
}
.text-bx h1{
    font-size: 3rem;
    text-transform: uppercase;
}
.text-bx h1 b{
    color: #f1676d;
}
.text-bx p{
    color: #372c62;
    font-weight: 400;
    margin-top: 20px;
}
.text-bx .input-bx{
    margin: 20px;
    display: flex;
}
.text-bx .input-bx input{
    width: 60%;
    display: block;
    height: 50px;
    padding: 10px;
    border: none;
    outline: none;
    color: #8997b9;
    font-size: 16px;
}
.text-bx .input-bx input::placeholder{
    color: #8997b9;
}
.text-bx .input-bx button{
    outline: none;
    border: none;
    padding: 10px 20px;
    background-color: #5654b3;
    color: white;
    font-size: 15px;
}
.midias-sociais{
    margin-top: 30px;
}
.midias-sociais a{
    text-decoration: none; 
}
.midias-sociais i{
      font-size: 23px;
      margin: 0 3px;
      color: white;
      background-color: #372c62;
      padding: 7px;
      border-radius: 5px;
}
.img-bx{
    width: 60%;
}
.img-bx img{
    width: 100%;
}
@media (max-width:970px){
    nav .menu-icon{
        display: block;
    }
    nav ul{
        position: fixed;
        width: 60%;
        height: 100%;
        top: 0;
        left: 0;
        transform: translateX(-100%);
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        transition: 0.3s ease-in;
        background-color: #5654b3;
    }
    nav ul.active{
        transform: translateX(0);
    }
    nav ul li{
        padding: 10px;
    }
    nav ul li a{
        font-size: 18px;
        color: white;
    }
    nav ul button{
        background-color: #f1676d;
        font-size: 18px;
        margin: 10px;
    }
    main{
        flex-direction: column;
    }
    .text-bx,
    .img-bx{
        width: 100%;
        text-align: center;
    }
    .text-bx{
        margin-bottom: 40px;
    }
    .text-bx .input-bx{
        justify-content: center;

    }
}
var menu = ducument.querySelector('nav ul');
var menuBar = document.querySelector('nav .menu-icon');
var iconMenu = document.querySelector('nav .menu-icon img');

menuBar.addEventListener('click',function(){
     menu.classList.toggle('active');
});

