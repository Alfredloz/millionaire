<template>
    <div class="answer_box">
        <h3>Seleziona una delle risposte</h3>
        <div class="single_answer d_flex">
            <p v-for="(answer, i) in questionSelected.answers" :key="answer.key" @click="rightAnswer(i)" :class="{'rightAnswer': 'right_color'}">{{ answer.title }}</p>
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
      counter: false,
    }
  },
  methods:{
    rightAnswer(index){
        if (this.questionSelected.answers[index].correct === true) {
        
            this.counter= true;
            console.log(this.counter);
        } else{
            this.counter = false;
            console.log(this.counter);

        }
    //   console.log(this.questionSelected.answers[index].correct);
    }
  }
}
</script>