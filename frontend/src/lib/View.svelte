<script lang="ts">

</script>
<style>
   

   .question-container {
    border: 1px solid var(--button-color);
    border-radius: 0.5rem;
    padding: 15px;
    margin-bottom: 20px;
    text-align: left;
    }

    p {
    font-size: 18px;
    margin-bottom:20px;
 
    }

    .option {
    
    padding: 10px 20px;
    width: 95%;
    text-align: left;
    margin-bottom: 0.5rem;
    border-radius: 5px;
    

    }

    #option1{
        background-color: rgb(205, 246, 205);
        color: green;
    }

    #option2{
        background-color: rgb(246, 205, 213);
        color: red;
     
    }
</style>

<div class="question-container">
    <p>1. What time will you go to the museum?</p>
    <div class="options">
      <div class="option" id="option1">1pm in the morning</div>
      <div class="option" id="option2">2pm in the afternoon</div>
    </div>
</div>