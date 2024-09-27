<script lang="ts">

</script>
<style>
    .quiz-card {
        border: 2px solid var(--button-color);
        border-radius: 10px;
        padding: 20px;
        margin-bottom: 20px;
    }

    .question {
        font-size: 16px;
        font-weight: bold;
        margin-bottom: 20px;
    }

    .answers {
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
    }

    .option {
        display: flex;
        align-items: center;
        margin-bottom: 15px;
        width: 48%;
    }

    input[type="radio"] {
        display: none;
    }

    .circle {
        display: inline-block;
        width: 40px;
        height: 40px;
        border-radius: 50%;
        border: 1px solid var(--button-color);
        color: var(--button-color);
        font-weight: bold;
        text-align: center;
        line-height: 40px;
        margin-right: 10px;
    }

    input[type="radio"]:checked + .circle {
        background-color: var(--button-color);
        color: white;
    }

    .answer-text {
        font-weight: bold;
    }

    .button-container {
        display: flex;
        justify-content: space-around;
    } 
</style>


<div class="quiz-card">
    <p class="question">1. How many kinds of questions are there in the list?</p>
    <div class="answers">
        <label class="option">
            <input type="radio" name="question1" value="A">
            <span class="circle">A</span> 
            <span class="answer-text">two</span>
        </label>
        <label class="option">
            <input type="radio" name="question1" value="B">
            <span class="circle">B</span> 
            <span class="answer-text">three</span>
        </label>
        <label class="option">
            <input type="radio" name="question1" value="C">
            <span class="circle">C</span> 
            <span class="answer-text">four</span>
        </label>
        <label class="option">
            <input type="radio" name="question1" value="D">
            <span class="circle">D</span> 
            <span class="answer-text">five</span>
        </label>
    </div>
</div>