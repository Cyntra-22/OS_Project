<script lang="ts">
    import QuizScore from "$lib/QuizScore.svelte";
    const quizzes = Array(5).fill({});

</script>
<style>

    .profile-container {
        width: 80%;
        margin: 0 auto;
        background-color: white;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    }

    .profile-card {
        display: grid;
        grid-template-columns: repeat(2,1fr);
        align-items: center;
        border: 2px solid var(--button-color);
        border-radius: 10px;
        margin-bottom: 20px;
    }

    .profile-image img {
        width: 180px;
        height: 180px;
        padding-left: 200px;
        border-radius: 50%;
        margin-right: 20px;
    }

    .profile-info {
        text-align: left;
    }

    .profile-name {
        font-size: 18px;
        font-weight: bold;
    }

    .profile-email, .profile-phone {
        font-size: 16px;
        color: gray;
        margin-top: 5px;
    }

    .quiz-list {
        border: 2px solid var(--button-color);
        border-radius: 10px;
        padding: 10px;
    }

   

</style>
    <div class="profile-container">
        <div class="profile-card">
            <div class="profile-image">
                <img src="/profile.jpg" alt="User Image">
            </div>
            <div class="profile-info">
                <p class="profile-name">Myo Pa Pa Kyaw</p>
                <p class="profile-email">myopapakyaw147@gmail.com</p>
                <p class="profile-phone">09 45073029</p>
            </div>
        </div>
        
        <div class="quiz-list">
            {#each quizzes as quiz, index}
                <QuizScore/>
            {/each}
        </div>
    </div>


