// classe chamada NegociacaoController, que será responsável por capturar dados de um formulário, como data, quantidade e valor, e criar uma instância de negociação.

import { Negociacao } from "../models/negociacao.js";

export class NegociacaoController{
    private inputData: HTMLInputElement;
    private inputQuantidade: HTMLInputElement;
    private inputValor: HTMLInputElement;


    constructor(){
        this.inputData= document.querySelector('#data');
        this.inputQuantidade= document.querySelector('#quantidade'); 
        this.inputValor= document.querySelector('#valor');   
    }
    // O método adicionar() é responsável por adicionar uma nova negociação à lista de negociações. Ele utiliza os métodos querySelector para       
        adicionar() {
            const exp = /-/g;

            const date = new Date(this.inputData.value.replace(exp, ','));
            const quantidade = parseIntgit remote add origin https://github.com/jmolima744/typs_12-04-2025.git(this.inputQuantidade.value);
            const valor = parseFloat(this.inputValor.value);
            // O método replace() é utilizado para substituir todas as ocorrências de um padrão (neste caso, o padrão é -) por uma nova string (neste caso, a nova string é ,).
            // console.log(this.inputData);
            // console.log(this.inputQuantidade);
            // console.log(this.inputValor);
            const negociacao = new Negociacao(date,quantidade, valor);
                // this.inputData.value,
                // this.inputQuantidade.value,
                // this.inputValor.value
            // );
            console.log(negociacao);
        }
}
