const resultado=document.querySelector(".display");
const armazenandoValor=document.querySelector('#armazenando');
const zerandoResultado=document.querySelector('#apagando_tudo');
const apagandoTudoDisplay=document.querySelector('#apagando_numeros');
const apagandoNumeroDisplay=document.querySelector('#apagando_numero');
const somandoValores=document.querySelector('#somando_valores');

// Atualiza no visor após a opção escolhida pelo usuário;
function escrevendoValoresNoVisor(){
    mesclandoValores=pegandoValores.join('');
    mesclandoValores=Number(mesclandoValores);
    resultado.innerHTML = mesclandoValores;
}

// função que reserva o valor do usuário;
function reservandoValor(){
    mesclandoValores=pegandoValores.join('');
    mesclandoValores=Number(mesclandoValores);
    armazenandoValoresParaSoma.push(mesclandoValores);
}

// função de soma do programa;
function funcaoSoma(valor01,valor02){
    const somando = valor01+valor02;
    return somando;
}


// valor padrão do visor.
resultado.innerHTML = 0; 


// irá armazenar os ID dos butões.
const variaveis = ['#zero','#um','#dois','#tres','#quatro','#cinco','#seis','#sete','#oito','#nove']; 

// irá armazenar os valores digitados do usuário;
let pegandoValores = [];

// após o usuário clicar em reservar valor, ele irá para este array, capacidade de 2 valores de até 15 números;
let armazenandoValoresParaSoma = [];

// Variável que recebe o valores, e mescla eles.
let mesclandoValores;


let valor01; // usado na função de soma;
let valor02; // usado na função de soma
let armazenandoResultadodoVisor; // exibe resultado da operação na tela;

const butoes = []; // Array que agiliza a criação dos eventos captados;

for(let i=0; i<variaveis.length; i++){
    butoes.push(document.querySelector(variaveis[i]));
    butoes[i].addEventListener("click", function(e){ // criando o evento para pegar o valor digitado pelo usuário;
        e.preventDefault();
        pegandoValores.push(i);
        mesclandoValores=pegandoValores.join('');
        mesclandoValores=Number(mesclandoValores);
        while(pegandoValores.length == 15   ){
            pegandoValores.pop(i);
        }
        resultado.innerHTML = mesclandoValores;
        apagandoTudoDisplay.addEventListener("click", function(e){ // apaga todo o valor digitado pelo usuário, resetando as variáveis;
            e.preventDefault();
            pegandoValores.pop(i);
            escrevendoValoresNoVisor();
        })
    })
}

// Apaga um número digitado erroneamente pelo usuário;
apagandoNumeroDisplay.addEventListener("click", function(e){
    e.preventDefault();
    pegandoValores.pop();
    escrevendoValoresNoVisor();
})

// Evento que armazena o valor digitado pelo usuário;
armazenandoValor.addEventListener("click", function(e){
    e.preventDefault();
    reservandoValor();
    resultado.innerHTML = 0;
    console.log(armazenandoValoresParaSoma);
    mesclandoValores = "";
    pegandoValores = [];
})

// Evento que exibe o resultado da soma, dos valores digitado pelo usuário;
somandoValores.addEventListener("click", function(e){
    e.preventDefault();
    valor01=armazenandoValoresParaSoma[0];
    valor02=armazenandoValoresParaSoma[1];
    armazenandoResultadodoVisor = funcaoSoma(valor01,valor02);
    resultado.innerHTML = armazenandoResultadodoVisor;
})

// Após toda operação realizada, esse evento deve acontecer para resetar as variáveis e possibilitar uma nova operação;
zerandoResultado.addEventListener("click", function(e){
    e.preventDefault();
    armazenandoValoresParaSoma = [];
    pegandoValores = [];
    mesclandoValores = "";
    resultado.innerHTML = 0;
});





