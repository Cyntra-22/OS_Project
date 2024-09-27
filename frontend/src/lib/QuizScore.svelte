<script lang="ts">

</script>
<style>
     .quiz-item {
        display: grid;
        grid-template-columns: 3fr 3fr 3fr 3fr;
        align-items: center;
        margin-bottom: 10px;
    }

    .quiz-item div{
        border-right: 1px solid var(--button-color);
        text-align: center;
        font-size: 17px;
    }

    .quiz-item div:last-child {
        border-right: none;
    }

    .quiz-title {
        font-size: 16px;
        font-weight: bold;
    }

    .result{
        color: var(--button-color);
    }
    button{
        border: none;
    }

    button:hover{
        color: var(--button-color);
    }

    .view-btn, .del-btn {
        padding: 5px 10px;
        background-color: white;
        cursor: pointer;
        margin-left: 10px;
        font-size: 17px;
    }

    .quiz-score {
        margin-left: 10px;
        font-weight: bold;
    }

    .divider {
        border: none;
        height: 1px;
        background-color: lightgray;
        margin: 10px 0;
    }
</style>

<div class="quiz-item">
    <div class="quiz-title">Quiz 1</div>
    <div>
        <button class="view-btn">View</button>
    </div>
    <div>
        <button class="del-btn">Del</button>
    </div>
    <div>
        <p class="quiz-score"><span class="result">5 </span> / 10</p> 
    </div>   
</div> 
<hr class="divider"> 