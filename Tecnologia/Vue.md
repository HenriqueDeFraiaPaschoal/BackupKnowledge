# Vue

## O que é?

## Como funciona?

## Estruturação

## Boas práticas


atributos
v-once ---> O elemento é renderizado apenas uma vez, ele não sofre mudanças
v-model ---> 

v-on ---> pode ser substituido por @ no começo do atributo
v-bind ---> pode ser substituido or : no começo do atributo

Como passar um valor pelo script do vue para o html

// Script do vue dentro do head
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>


<h1>{{ chave }}<h1>

<script>
	const { createApp } = Vue;
	
	createApp({
		data(){
			return {
			chave:valor
			}
		}
	}).mount("#App");

</script>
