<template>
    <div class="question_box">
        <h2>Rispondi alla domanda</h2>
        <p >{{ questionSelected.question }}</p>
        
    </div>
</template>
<script>
export default {
    name:'QuestionComponent',
    props:{
        questionSelected: null,
    }
}
</script>