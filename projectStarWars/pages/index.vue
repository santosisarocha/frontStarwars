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
        <h1 class="apitext">API</h1>
        <h2 class="trip-details">Trip Details of ID: {{ $route.params.id }}</h2>
        <div class="details" v-if="Object.keys(characters).length">
            <p><strong>Nome:</strong> {{ characters.name }}</p>
            <p><strong>Height:</strong> {{ characters.height }}</p>
        </div>
        <div class="character-search">
            <h3>Do you want another character?</h3>
            <label for="character-id">Character ID:</label>
            <input id="character-id" v-model="character" type="number">
            <button v-on:click="getCharacter">Find</button>
        </div>
        <div v-if="Object.keys(characters).length">
            <p>Vai se fuder {{ characters }}</p>
        </div>
    </div>
            <button class="get">GET</button>
            <button class="post">POST</button>
            <button class="put">PUT</button>
            <button class="del">DEL</button>
        </div>
        
    </div>
</template>

<script setup>
    const route = useRoute();
    console.log("route", route);
    const character = ref('');
    const characters = ref({});
    
    const getCharacter = async () => {
        const { data: peopleFound} = await useFetch(`https://swapi.dev/api/people/${character.value}`);
        characters.value = peopleFound._value;
    }

</script>


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
    .api {
        height: 500px;
        width: 650px;
        background-color: rgba(50, 50, 46, 0.85);
        position: absolute;
        z-index: 5;
        top: 650px;
        left: 600px;
        border-radius: 30px;
        padding: 20px;
        color: white;
    }

    .apitext {
        text-align: center;
        font-size: 30px;
        margin-bottom: 20px;
        
    }

    .trip-details {
        font-size: 24px;
        margin-bottom: 20px;
        background-color: rgba(50, 50, 46, 0.85);
    }

    .details p {
        z-index: 2;
        margin-bottom: 10px;
        background-color: rgba(50, 50, 46, 0.85);
    }

    .character-search {
        margin-top: 20px;
        background-color: rgba(50, 50, 46, 0.85);
    }

    .character-search h3 {
        margin-bottom: 10px;
        background-color: rgba(50, 50, 46, 0.85);
    }

    .character-search label {
        margin-right: 10px;
        background-color: rgba(50, 50, 46, 0.85);
    }

    .character-search input {
        padding: 5px;
        border-radius: 5px;
        border: 1px solid #ccc;
        margin-right: 10px;
        background-color: rgba(50, 50, 46, 0.85);
    }

    .character-search button {
        padding: 5px 10px;
        border-radius: 5px;
        background-color: rgb(252, 192, 0);
        color: white;
        border: none;
        cursor: pointer;
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
