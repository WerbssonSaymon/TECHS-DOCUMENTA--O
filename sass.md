Sass é um pré-processador CSS

Tem duas extensões
.scss - mesma sintaxe do css
.sass - que é a sintaxe recuada sem o uso de chaves


Declaração de variaveis

$cor1: rgb(182, 29, 29);
$cor2: rgb(113, 113, 243);
$cor3: rgb(20, 98, 20);
$cor4: rgb(0,0,0);
$cor5: rgb(255, 255, 255);
$px1: 16px;
$px2: 20px;
$px3: 24px;
$px4: 30px;
$px5: 40px;
$largura: 100vw;
$altura: 25vh;

Exemplo de aninhamento do SASS

header {
    background-color: $cor1;
    width: $largura;
    height: $altura;

    h1 {
        color: $cor5;

        &:hover {
            font-size: $px5;
        }

    }
}
main {
    background-color: $cor2;
    width: $largura;
    height: $altura;
}

Modularisação do Sass
É onde pego um arquivo sass externo para colocar no arquivo principal

Chamada
@import 'modulo_footer';

Arquivo modulo_footer
footer {
    background-color: aqua;
    width: 100vw;
    height: 25vh;
    border: solid 3px whitesmoke;
    border-radius: 25px;
}

Mixin
É um bloco de instrução

Parametros dentro do mixin chamado bloco

@mixin bloco($cor: yellow, $contorno: 25px){ 

    width: 200px;
    height: 200px;
    background-color: $cor;
    border-radius: $contorno;
    margin: 10px;

}

Inclusao do mixin

.div1 {
    @include bloco();
}
.div2 {
    @include bloco($cor: orange);
}
.div3 {
    @include bloco($cor: rgb(19, 139, 19), $contorno: 100px);
}

Conceito de herança no sass com extend 

.texto {
    margin-left: 15px;
    font-size: 20px;

    &--linha1 {
        @extend .texto;
        color: blueviolet;
    }

    &--linha2 {
        @extend .texto;
        color: deepskyblue;
    }
}