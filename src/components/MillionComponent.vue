<template>
    <div class="million_box"  v-bind:randomQuestion="randomQuestion()">
    <QuestionComponent :questionSelected="questionSelected" />
    <AnswerComponent :questionSelected="questionSelected"/>
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
                        key:1,
                        title: 'rosso',
                        correct: false
                    },
                    {
                        key:2,
                        title: 'verde',
                        correct: false
                    },
                    {
                        key:3,
                        title: 'azzurro',
                        correct: false
                    },
                    {
                        key:4,
                        title: 'bianco',
                        correct: true
                    }
                ]
            },
            {
                question: 'Quale di questi libri è di Daniele Biacchesse',
                answers:[
                    {
                        key:1,
                        title: 'American Gods',
                        correct: false
                    },
                    {
                        key:2,
                        title: 'La collina dei conigli',
                        correct: false
                    },
                    {
                        key:3,
                        title: 'Il signore degli Anelli',
                        correct: false
                    },
                    {
                        key:4,
                        title: `'L'altra America di Woody Guthrie`,
                        correct: true
                    }
                ]
            },
            {
                question: `Quand'è stata messa in vendita in Italia la Nintendo Enterteiment System? `,
                answers:[
                    {
                        key:1,
                        title: '15 luglio 1983',
                        correct: false
                    },
                    {
                        key:2,
                        title: '18 ottobre 1985',
                        correct: false
                    },
                    {
                        key:3,
                        title: '1º settembre 1986',
                        correct: false
                    },
                    {
                        key:4,
                        title: '30 novembre 1987',
                        correct: true
                    }
                ]
            },
            {
                question: `Quand'è stato pubblicato l'album Black Sabbath del gruppo musicale omonimo?`,
                answers:[
                    {
                        key:1,
                        title: '16 febbraio 1984',
                        correct: false
                    },
                    {
                        key:2,
                        title: '18 agosto 1942',
                        correct: false
                    },
                    {
                        key:3,
                        title: '1º dicembre 2001',
                        correct: false
                    },
                    {
                        key:4,
                        title: '13 febbraio 1970',
                        correct: true
                    }
                ]
            },
            {
                question: `In quale canto della Divina Commedia viene introdotto la figura del Conte Ugolino della Gheradesca?`,
                answers:[
                    {
                        key:1,
                        title: 'nel canto X del Purgatorio',
                        correct: false
                    },
                    {
                        key:2,
                        title: `Nel canto IV dell'inferno`,
                        correct: false
                    },
                    {
                        key:3,
                        title: 'nel canto II del Paradiso ',
                        correct: false
                    },
                    {
                        key:4,
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
            // console.log(this.questionSelected); 
        }
    },
}
</script>
