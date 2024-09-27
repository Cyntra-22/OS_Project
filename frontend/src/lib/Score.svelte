<script>
    import { goto } from "$app/navigation";

    function handleAlert(){
        alert("Your Quiz is successfully saved.")
    }
    function handleNewQuiz(){
        goto('/');
    }
</script>
<style>

    .container {
        border-radius: 10px;
        box-shadow: 0 4px 12px rgba(55, 17, 17, 0.1);
        margin: 0 auto;
        width:65%;
        padding: 2rem;
        margin-top: 4.5rem;
        text-align: center;
        background-color: white;
    }


    img{
    
        width: 250px;
        height: 250px;
        margin: 0 auto 20px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    h1 {
        color: var(--button-color);
        font-size: 30px;
        margin-bottom: 20px;
    }


    .score-title {
      
        font-size: 25px;
        margin-bottom: 10px;
    }

    .score {
        font-size: 28px;
        font-weight: bold;
        margin-bottom: 20px;
    }

    .message {
        font-size: 18px;
        margin-bottom: 20px;
    }

    .result-score{
        color: var(--button-color);
    }

    .button-container {
        display: flex;
        justify-content: space-around;
        margin-top: 2rem;
    }

    .btn {
        padding: 12px;
        background-color: hsl(5, 85%, 63%);
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 17px;
    }

    .btn:hover{
        background-color: white;
        border: 1px solid var(--button-color);
        color: var(--button-color);
    }

    .save-btn {
        width: 35%;
    }

    .generate-btn {
        width: 35%;
    }

</style>

<div class="container">
    <div class="image-box">
        <img src="/congratulation.png" alt="congratulation">
    </div>
        <h1>CONGRATULATIONS!</h1>
        <p class="score-title">Your Score</p>
        <p class="score"><span class="result-score">4</span> / 10</p>
        <p class="message">You did a great job, learn more by taking another quiz.</p>
    <div class="button-container">
        <button class="btn save-btn" on:click={handleAlert}>Save the Quiz</button>
        <button class="btn generate-btn" on:click={handleNewQuiz}>Generate new Quiz</button>
    </div>
</div>
