<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    
</head>
<style>
    *{
        margin: 0px;
        padding: 0px;
    }
    body{
       display: flex;
       min-height: 100vh;
       justify-content: center;
       align-items: center;
       background: black;
       color: azure;
       gap: 5vw;
    } 
    .animated-card,
    .animated-card2{
        display: grid;
        place-items: center;
        position: relative;
        height: 500px;
        width: 350px;
        background: #222;
        border-radius: 10px;
        cursor: pointer;
    }
    h1{
        color:rgba(254,254,144,0,1);
        text-decoration: none;
        font-size: 25px;
        z-index: 10;
    }
    .animated-card::before{
        position: absolute;
        content: '';
        height: 500px;
        width: 350px;
        background: orange;
        border-radius: 10px;
        z-index: -1;
        transition: 3;
        animation: animate 2s linear infinite;
    }
    .animated-card:hover::before{
        height: 512px;
        width: 362px;

    }
    @keyframes animate{
        50%{
            filter: hue-rotate(360deg);
        }
    }
    /* Secound card */

    .animated-card2::before{
        position: absolute;
        content: '';
        width: 50%;
        height: 100%;
        background: white;
        transform: rotate(45deg);
    }
    .animated-card2:hover::before{
        animation: animate2 2s linear infinite;
    }
    @keyframes animate2{
        from{
            transform: rotate(0deg);
        }
        to{
            transform: rotate(360deg);
        }
    }
    .animated-card2::after{
        position: absolute;
        content: '';
        inset: 5px;
        background: #222;
        border-radius: 8px;
    }
    
</style>
<body>
    <div class="animated-card">
      <h1 class="class-h1-first">Ola</h1>
    </div>
    <div class="animated-card2">
        <h1 class="class-h1-second">Ola 2</h1>
    </div>
</body>
</html>


[![Web](https://img.shields.io/badge/website-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://trialofmidgard.com.br)



