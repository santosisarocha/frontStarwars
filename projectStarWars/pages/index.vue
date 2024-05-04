<template>
    <header>
        <h1>Home</h1>
        <a href="http://127.0.0.1:5500/nave.html" target="_blank">Jogo</a>
        <h1>Courses</h1>
        <input type="text" placeholder="Search in site">
    </header>
    <div class="capa">
        <img class="capaImg" src="../assets/capa.png">
    </div>
    <div >
        <div>
            <img class="fundoImg" src="../assets/fundo.png">
            <div class="api">
                <H1 class="apitext">API</H1>
            </div>
            <button class="get">GET</button>
            <button class="post">POST</button>
            <button class="put">PUT</button>
            <button class="del">DEL</button>
        </div>
        
    </div>
</template>

<style scoped>
    
    header {
        background-color: black;        
        display: flex;        
        align-items: center; 
        justify-content: center; 
        height: 70px;
    }
    
    h1 {
        margin-left: 10px;
        margin-right: 100px;
        color: rgb(252, 192, 0);
        font-size: 25px;
        font-style:initial;
    }
    a {
        margin-left: 10px;
        margin-right: 100px;
        color: rgb(252, 192, 0);
        font-size: 25px;
        font-style:initial;
    }
    input {
        padding: 5px; 
        border-radius: 7px;
        background-color: black;
        border-bottom: black;
        color: rgb(252, 192, 0);
    }
    
    .capaImg{
        width: 100%;        
        position: absolute;
        z-index: 1;
        
    }
    .fundoImg{
        width: 100%;        
        position: absolute;
        height: 1400px;
                
    }
    div{
        background-color: black;
        
    }
    .api{
        height: 500px;
        width: 650px;
        background-color: rgb(50, 50, 46, 0.85);
        position: absolute;
        z-index: 5;
        margin-top: 650px;
        margin-left: 600px;
        border-radius: 30px;
    }
    .apitext{
        margin-left: 45%;
        margin-top: 10%;
        font-style:initial;
    }
    button{
        position: absolute;
        z-index: 10;
    }

    .get{
        margin-top: 68%;
        margin-left: 32%;
        width: 120px;
        height: 70px;
        background-color: rgb(252, 192, 0);
        color: white;
        border-radius: 15px;
    }
    .post{
        margin-top: 68%;
        margin-left: 42%;
        width: 120px;
        height: 70px;
        background-color: rgb(252, 192, 0);
        color: white;
        border-radius: 15px;
    }
    .put{
        margin-top: 68%;
        margin-left: 52%;
        width: 120px;
        height: 70px;
        background-color: rgb(252, 192, 0);
        color: white;
        border-radius: 15px;
    }
    .del{
        margin-top: 68%;
        margin-left: 62%;
        width: 120px;
        height: 70px;
        background-color: rgb(252, 192, 0);
        color: white;
        border-radius: 15px;
    }
    
    
</style>
