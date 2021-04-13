<template>
    <div class="million_box">
        <h1>Ciao</h1>
        <h2 @click="randomQuestion()">ciao due</h2>
    <QuestionComponent v-bind:selectedQuestion="selectedQuestion" />
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
            },
            {
                question: `Quand'è stata messa in vendita in Italia la Nintendo Enterteiment System? `,
                answers:[
                    {
                        title: '15 luglio 1983',
                        correct: false
                    },
                    {
                        title: '18 ottobre 1985',
                        correct: false
                    },
                    {
                        title: '1º settembre 1986',
                        correct: false
                    },
                    {
                        title: '30 novembre 1987',
                        correct: true
                    }
                ]
            },
            {
                question: `Quand'è stato pubblicato l'album Black Sabbath del gruppo musicale omonimo?`,
                answers:[
                    {
                        title: '16 febbraio 1984',
                        correct: false
                    },
                    {
                        title: '18 agosto 1942',
                        correct: false
                    },
                    {
                        title: '1º dicembre 2001',
                        correct: false
                    },
                    {
                        title: '13 febbraio 1970',
                        correct: true
                    }
                ]
            },
            {
                question: `In quale canto della Divina Commedia viene introdotto la figura del Conte Ugolino della Gheradesca?`,
                answers:[
                    {
                        title: 'nel canto X del Purgatorio',
                        correct: false
                    },
                    {
                        title: `Nel canto IV dell'inferno`,
                        correct: false
                    },
                    {
                        title: 'nel canto II del Paradiso ',
                        correct: false
                    },
                    {
                        title: `nel canto XXXIII dell'Inferno`,
                        correct: true
                    }
                ]
            }
           ],
        //    variabile con la domanda random
           questionSelected: null,
       }
    },
    methods: {
        randomQuestion(){
            const i = Math.floor(Math.random() * this.questionsArray.length);

            this.questionSelected = this.questionsArray[i];
            console.log(this.questionSelected); 
        }
    },
}
</script>
