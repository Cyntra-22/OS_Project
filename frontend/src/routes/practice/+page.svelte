<script lang="ts">
    import Practice from "$lib/Practice.svelte";
    import { goto } from "$app/navigation";

    let questions = Array(5).fill(null);

    function handleSubmitAnswers(event: Event){
        event.preventDefault();
        goto('/score');
    }

</script>
<style>

    .main-container{
        width: 80%;
        margin: 0 auto;
    }

    .quiz-container {
        
        background-color: white;
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }

    h1 {
        margin-bottom: 20px;
        text-align: center;
    }

   .button-container{
        display: flex;
        justify-content: space-around;
   }

    .btn {
        padding: 10px 20px;
        background-color: var(--button-color);
        border: none;
        border-radius: 5px;
        color: white;
        font-size: 18px;
        cursor: pointer;
        margin-top: 20px;
        width: 40%;
        
    }

    .clear-btn {
        background-color: var(--button-color);
    }

    .btn:hover {
        background-color: white;
        border: 1px solid var(--button-color);
        color: var(--button-color);
    }

</style>
<div class="main-container">
    
    <form action="/your-backend-endpoint" method="POST" on:submit={handleSubmitAnswers}> 
        <div class="quiz-container">
            <h1>Welcome To Our Quiz</h1> 
           
                <Practice />
      
        </div>

        <div class="button-container">
            <button type="reset" class="btn clear-btn">Clear Your Answers</button>
            <button type="submit" class="btn submit-btn">Submit Your Answers</button>
        </div>
    </form>
</div>
    
