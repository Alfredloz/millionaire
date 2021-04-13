<template>
    <div class="answer_box">
        <h3>Seleziona una delle risposte</h3>
        <p v-for="answer in questionSelected.answers" :key="answer.key">{{ answer.title }}</p>
    </div>
</template>
<script>
export default {
    name:'AnswerComponent',
    props: {
        questionSelected: null
    }
}
</script>