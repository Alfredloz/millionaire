<template>
    <div class="million_box">
        <h1 @click="clickFun()">Ciao</h1>
        <h2>ciao due</h2>
    <QuestionComponent v-bind:questionsArray="questionsArray" />
    <AnswerComponent/>
    </div>
</template>
<script>
// nesting components
import QuestionComponent from './QuestionComponent'
import AnswerComponent from './AnswerComponent'
export default {
    name:'MillionComponent',
    components:{
        QuestionComponent,
        AnswerComponent
    },
    data(){
       return {
           questionsArray:[
            {
                question: 'Di che colore è il cavallo bianco di napoleone?',
                answers:[
                    {
                        title: 'rosso',
                        correct: false
                    },
                    {
                        title: 'verde',
                        correct: false
                    },
                    {
                        title: 'azzurro',
                        correct: false
                    },
                    {
                        title: 'bianco',
                        correct: true
                    }
                ]
            },
            {
                question: 'Quale di questi libri è di Daniele Biacchesse',
                answers:[
                    {
                        title: 'American Gods',
                        correct: false
                    },
                    {
                        title: 'La collina dei conigli',
                        correct: false
                    },
                    {
                        title: 'Il signore degli Anelli',
                        correct: false
                    },
                    {
                        title: `'L'altra America di Woody Guthrie`,
                        correct: true
                    }
                ]
            }
           ]
       }
    },
    methods: {
        clickFun(){
            console.log(this.array);
        }
    },
}
</script>
