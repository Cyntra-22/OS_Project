<script lang="ts">
    import View from "$lib/View.svelte";


</script>
<style>
    .view-mode {

    width: 80%;
    margin: 5rem auto;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(55, 17, 17, 0.1);
    text-align: center;

    }

    h1 {
    font-size: 24px;
    margin-bottom: 20px;
    }


  
    button {
        padding: 12px 40px;
        border: none;
        border-radius: 5px;
        font-size: 1rem;
        cursor: pointer;
        color: #fff;
        background-color: hsl(5, 85%, 63%);
        margin-top: 10px;
        
    }

    button:hover {
        background-color: hsl(5, 67%, 52%);
    }



</style>

<div class="view-mode">
    <h1>View Mode</h1>
    <View/>
    <View/>
    <button class="retake-quiz">Retake Quiz</button>
  </div>
  