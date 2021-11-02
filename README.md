# project flexbox DIO

#html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex Turismos</title>
    <link rel="stylesheet" href="./style.css">
</head>
<body>
    <header>
        <div class="flex-container menu">
            <div><h1>FlexTurismos</h1></div>
            <ul class="list-items">
                <li><a href="#quem-somos">Quem Somos</a></li>
                <li><a href="#servicos">Serviços</a></li>
                <li><a href="#planos">Planos</a></li>
              </ul>  
        </div>
    </header>

    <div class="flex-container apresentacao">
            <div class="texto-apresentacao">
                <h1>Flex <br>Turismos</h1>
                <p>O melhor serviço para você!</p>
                <a href="" class="btn">Saiba Mais!</a>
            </div>
    
        <div>
            <div><img src="./images/0-main.png" alt="banner de apresentação"></div>
        </div>
    </div>

    <div class="flex-container" id="quem-somos">
        <div>
            <h2>Quem somos</h2>
            <p>It is a long established fact that a reader will be distracted by the readable content of a page when looking at its layout. </p>
            <p>The point of using Lorem Ipsum is that it has a more-or-less normal distribution of letters, as opposed to using 'Content here, content here', making it look like readable English.</p>
        </div>
        <div>
            <img src="./images/1-quem-somos.png" alt="balcão de atendimento">
        </div>

    </div>

    <div class="container-externo">
        <div class="flex-container" id="servicos">
            <div>
                <h2>Serviços</h2>
            </div>

            <div class="list-servicos">
                <div class="item-servico" >
                    <div><img src="./images/icon-2.png" alt="hospedagens"></div>
                    <p>Hospedagens</p>
                    <a href="#">Comprar Agora</a>
                </div>

                <div class="item-servico">
                    <div><img src="./images/icon-1.png" alt="pacote de viagens"></div>
                    <p>Pacotes de viagens</p>
                    <a href="#">Comprar Agora</a>
                </div>

                <div class="item-servico">
                    <div><img src="./images/icon-3.png" alt="roteiros personalizados"></div>
                    <p>Roteiros personalizados</p>
                    <a href="#">Comprar Agora</a>
                </div>

            </div>
        </div>
    </div>

    <div class="flex-container" id="planos">

        <div><h2>Planos</h2></div>

        <div class="list-planos">
            <div class="item-plano">
                <h3>Plano 1</h3>
                    <ul>
                        <li>Suporte 24h</li>
                        <li>Serviços de quarto</li>
                        <li>Guia turístico</li>
                    </ul>
                <a href="#" class="btn">Saiba Mais!</a>
            </div>
            <div class="item-plano">
                <h3>Plano 2</h3>
                <br>    
                    <ul>
                        <li>Suporte 24h</li>
                        <li>Serviços de quarto</li>
                        <li>Guia turístico</li>
                        <li>Roteiro de trilhas</li>
                    </ul>
                <a href="#" class="btn">Saiba Mais!</a>
            </div>
            <div class="item-plano">
                <h3>Plano 3</h3>
                <br>
                    <ul >
                        <li>Suporte 24h</li>
                        <li>Serviços de quarto</li>
                        <li>Guia turístico</li>
                        <li>Roteiro de trilhas</li>
                        <li>Serviço personalizado</li>
                        <li>Área Vip</li>
                    </ul>
                <a href="#" class="btn">Saiba Mais!</a>
            </div>
        </div>
    </div>

    <footer>
        <div class="flex-container footer">
            <p>&copy; 2021 CSS Flexbox</p>
            <p>Desenvolvido por: Thaís Souza</p>
        </div>
    </footer>
</body>
</html>

#CSS
*{
    margin: 0;
    padding: 0;
    font-family: 'Open Sans', sans-serif;
}
ul{
    list-style: none;
    margin: 0;
    padding: 0;    
}

ul li a{
    text-decoration: none;
}

div img{
    display: block;
    width: 100%;
}

.flex-container{
    display: flex;
    max-width: 992px;
    margin: auto;
    width: 100%;
    min-width: 320px ;
   
}

header{
    background: rgba(2, 2, 2, 0.534);
    height: 100px;
    display: flex;
    align-items: center;
    color: #fff;
}

header .list-items{
    display: flex;
    max-width: 260px;
    width: 100%;
    justify-content: space-between;
    align-items: center;
}
.list-items li a{
    color: #fff;
}

header .menu{
    justify-content: space-between;
}
.apresentacao{
    height: 100vh;
    align-items: center;
    justify-content: space-between;
}
.apresentacao .texto-apresentacao{
    min-height: 200px;
    
    
}
.apresentacao .texto-apresentacao h1{
    color:rgba(2, 2, 2, 0.534) ;
    font-size: 48px;
    margin-bottom: 10px;
}

.btn{
    background-color: rgba(2, 2, 2, 0.534);
    color: #fff;
    text-align: center;
    border-radius: 30px;
    width: 220px;
    display: block;
    text-decoration: none;
    height: 30px;
    line-height: 30px;
   margin-top: 10px;
}

#quem-somos{
    flex-direction: row-reverse;    
    align-items: center;
    justify-content: space-between;
}

#quem-somos h2{
    font-size: 32px;
    color:rgba(2, 2, 2, 0.534);
    display: flex;
    margin-bottom: 20px;
}

#quem-somos h2::before{
    content: "";
    height: 50px;
    width: 5px;
    margin-right: 5px;
    background-color: rgba(2, 2, 2, 0.534);
    position: relative;
}
#quem-somos p{
    margin-bottom: 10px;
    width: 90%;
}
#quem-somos img{
    min-width: 440px;
}

.container-externo{
    background-color: rgba(2, 2, 2, 0.534);
    width: 100%;
}
#servicos{
    flex-direction: column;
    padding-top: 50px;
    padding-bottom: 100px;
}
#servicos h2{
    color: #fff;
    font-size:32px ;
    margin-bottom: 30px;
    
}

.list-servicos{
    
    display: flex;
    justify-content: space-between;
}
.list-servicos .item-servico{
        text-align: center;

}
.item-servico a{
    width: 220px;
    background-color: #fff ;
    border-radius: 30px ;
    height: 50px ;
    text-align: center;
    margin-top: 20px;
    line-height: 50px;
    padding: 5px 10px;
    color: rgba(2, 2, 2, 0.534);
    font-size: 12px;
    text-decoration: none;
    font-weight: 700;
}
.item-servico p{
    font-weight:700 ;
    font-size: 18px;
    color: #fff;
    margin-top: 20px;
}

.item-servico img{
    width: 80%;
    margin: auto;
}

#planos{
    flex-direction: column;
    min-height: 100vh;
    padding-top: 50px;
}
#planos h2{
    font-size: 32px;
    color: rgba(2, 2, 2, 0.534);
}

.list-planos{
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
}

.item-plano{
    flex: 1;
    border: 5px solid rgba(2, 2, 2, 0.534);
    padding: 10px;
    margin-right: 20px;
    max-width: 240px ;
   
}
.item-plano .btn{
    margin: auto;
    margin-bottom: 20px;
}
.item-plano h3{
    font-size: 24px;
    display: flex;
    flex-direction: column;
    text-align: center;
    color: rgba(2, 2, 2, 0.534);
    margin-top: 20px;
}
.item-plano h3::after{
    content: "";
    background-color: rgba(2, 2, 2, 0.534);
    width: 80%;
    height: 3px;
    margin-left: 25px;
    margin-top: 20px;
    margin-bottom: 10px;
}
.item-plano ul{
    padding: 10px 20px;
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;
}
.item-plano ul li{
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
}

.item-plano ul li::before{
    content: "";
    width: 10px;
    height: 10px;
    background-color: rgba(2, 2, 2, 0.534);
    margin-right: 5px;
}

footer{
    background-color: rgba(2, 2, 2, 0.534);
    height: 70px;
    display: flex;
    align-items: center;
}
footer .footer{
    justify-content: space-between;
    color: #fff;
}





/*mobile*/

@media(max-width: 992px)  {
    .flex-container{
        flex-direction: column;
    }
    .apresentacao{
        flex-direction: column-reverse;
        width:100%;
    }

    #quem-somos{
        flex-direction: column-reverse;
    }
    #quem-somos img{
        min-width: 320px;
        margin: auto;

    }


    .list-servicos{
        flex-direction: column;
    }
    .item-servico img{
        width: 50%;
        margin: auto;
    }
    .list-planos{
        flex-direction: column;
        align-items: flex-start;
        margin-bottom: 20px;
    }
    .list-planos .item-plano{
        max-width: 90%;
        padding: auto;
        width: 100%;
        margin-bottom: 20px;
    }
    
}
