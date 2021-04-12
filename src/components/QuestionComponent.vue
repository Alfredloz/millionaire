<template>
    <div class="question_box">
        <h2>lista dell'array</h2>
        <p v-for="question in questionsArray" :key="question.index">{{ question.question }}</p>
    </div>
</template>
<script>
export default {
    name:'QuestionComponent',
    props:{
        questionsArray: Array,
    }
}
</script>