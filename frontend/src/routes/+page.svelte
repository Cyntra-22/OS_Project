<script lang='ts'>
    import { goto } from "$app/navigation";

    function handleGenerate( event: Event){
        event.preventDefault();
        goto('/practice');
    }
</script>
<style>
    .container {
        width: 100%;
        margin: 0 auto;
        text-align: center;
    }

    h1 {
        font-size: 2.5em;
        margin-bottom: 5px;
        color: var(--button-color);
    }

    p {
        font-size: 1.4em;
        margin-bottom: 2rem;
        font-style: italic;

    }

    #quiz-form{
        border: 1px solid var(--button-color);
        border-radius: 1rem;
        padding: 3rem 1.5rem;
       
    }

    textarea {
        width: 95%;
        height: 250px;
        padding: 15px;
        font-size: 1rem;
        border: 1px solid #ccc;
        border-radius: 5px;
        resize: none;
        overflow-y: auto;
        margin-bottom: 20px;
    }

    .form-group {
        display: flex;
        justify-content: space-around;
        align-items: center;
        width: 100%;
    }

    select {
        width: 30%;
        padding: 10px;
        font-size: 1rem;
        border: 1px solid #ccc;
        border-radius: 5px;
        background-color: #f9f9f9;
    }

    button {
        padding: 0.7rem 2.5rem;
        font-size: 1rem;
        background-color:var(--button-color);
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    button:hover {
        background-color: #0056b3;
    }

    @media (max-width: 768px) {
        .form-group {
            flex-direction: column;
        }

        select, button {
            width: 100%;
            margin-bottom: 10px;
        }
        h1{
            font-size: 2rem;
        }
        p{
            font-size: 1.2rem;
        }
    }
</style>

<div class="container">
    <h1>Welcome To Quiz Portal!</h1>
    <p>"Can Generate Quiz and Practice"</p>
    
    <form id="quiz-form" on:submit={handleGenerate}>
        <textarea id="quiz-text" name="quiz-text" placeholder="Type Here..." rows="6"></textarea>
        
        <div class="form-group">
            <select id="num-questions" name="num-questions">
                <option value="" disabled selected>No of Questions</option>
                <option value="5">5 Questions</option>
                <option value="10">10 Questions</option>
                <option value="15">15 Questions</option>
                <option value="20">20 Questions</option>
            </select>
               
            <select id="difficulty" name="difficulty">
                <option value="" disabled selected>Difficulty Level</option>
                <option value="easy">Easy</option>
                <option value="medium">Medium</option>
                <option value="hard">Hard</option>
            </select>
            
            <button type="submit" >Generate ➔</button>
        </div>
    </form>
</div>