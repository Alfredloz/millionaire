<template>
    <div class="question_box">
        <h2>lista dell'array</h2>
        <p >{{ questionsArray[0].answers }}</p>
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