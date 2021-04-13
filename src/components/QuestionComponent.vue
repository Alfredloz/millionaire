<template>
    <div class="question_box">
        <h2>lista dell'array</h2>
        <p >{{ questionSelected }}</p>
    </div>
</template>
<script>
export default {
    name:'QuestionComponent',
    props:{
        questionSelected: String,
    }
}
</script>