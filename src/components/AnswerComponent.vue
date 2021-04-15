<template>
    <div class="answer_box">
        <h3>Seleziona una delle risposte</h3>
        <div class="single_answer d_flex">
            <p v-for="(answer, i) in questionSelected.answers" :key="answer.key" @click="rightAnswer(i)" v-bind:class="answer.correct == false ? 'wrong_color':'right_color'">{{ answer.title }}</p>
        </div>
    </div>
</template>
<script>
export default {
    name:'AnswerComponent',
    props: {
        questionSelected: null
    },
     data(){
    return{
      counter: 0,
    }
  },
  methods:{
    rightAnswer(index){
        if (this.questionSelected.answers[index].correct === true) {
            
            this.counter = 1;
            console.log(this.counter);
        } else{
            this.counter = 0;
        }
    //   console.log(this.questionSelected.answers[index].correct);
    }
  }
}
</script>