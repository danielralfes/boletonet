# Guia do Desenvolvedor

- [[Ajustar o tamanho da fonte do boleto bancário|GuiaDesenvolvedor#ajustar-o-tamanho-da-fonte-do-boleto-banc%C3%A1rio]]
- [[Ajustar a separação entre o símbolo da moeda e o valor|GuiaDesenvolvedor#ajustar-a-separa%C3%A7%C3%A3o-entre-o-s%C3%ADmbolo-da-moeda-e-o-valor]]
- [[Mostrar o endereço do Cedente|GuiaDesenvolvedor#mostrar-o-endere%C3%A7o-do-cedente]]

## Ajustar o tamanho da fonte do boleto bancário.

Para ajustar o tamanho da fonte utilize o método **AjustaTamanhoFonte** da classe **BoletoBancário**.

``` C#   
AjustaTamanhoFonte(double tamanhoFonteTextos = 10, 
                   double tamanhoFonteRotulos = 9.8, 
                   double tamanhoFonteInstrucaoImpressao = 9)
```      
 O tamanho da fonte será renderizada em "px" do css. 
``` css
.t { font-size: 9.8px !important; }
```

O método **AjustaTamanhoFonte** pode ser chamado antes ou depois do método **Valida**.

``` C#
        boletoBancario.Boleto = b;
        boletoBancario.Boleto.Valida();

        boletoBancario.AjustaTamanhoFonte(12, tamanhoFonteInstrucaoImpressao:14);
```

## Ajustar a separação entre o símbolo da moeda e o valor

Para ajustar a separação entre o símbolo da moeda e o valor utilize o método **AjustaSeparacaoSimboloMoeda** da classe **BoletoBancário**.

``` C#   
AjustaSeparacaoSimboloMoeda()
``` 

O método **AjustaTamanhoFonte** pode ser chamado antes ou depois do método **Valida**.

``` C#
        boletoBancario.Boleto = b;
        boletoBancario.Boleto.Valida();

        boletoBancario.AjustaSeparacaoSimboloMoeda();
```

[[https://github.com/BoletoNet/boletonet/blob/master/wiki/img/9207ef64-8de8-4fef-99fd-ef5ca3774316.png|alt=Ajustar separação entre o símbolo da moeda e o valor]]

## Mostrar o endereço do Cedente

Para mostrar o endereço do Cedente utilize a propriedade **MostrarEnderecoCedente** da classe **BoletoBancário**.

``` C#   
MostrarEnderecoCedente  = true;
``` 

É necessário preencher a propriedade **Endereco** da classe **Cedente**

``` C# 
            boletoBancario.Cedente.Endereco = new Endereco()
            {
                End = "Endereço do Cedente",
                Bairro = "Bairro",
                Cidade = "Cidade",
                CEP = "70000000",
                UF= "DF"

            };
```

Veja as imagens abaixo:

1. Sem o endereço do Cedente
[[https://github.com/BoletoNet/boletonet/blob/master/wiki/img/60665064-9f03-4ca9-a1de-43cedc88aa0c.PNG|alt=Sem o endereço do Cedente]]
2. Com o endereço do Cedente
[[https://github.com/BoletoNet/boletonet/blob/master/wiki/img/b7331994-6929-47c4-b7c1-57011e8d7794.PNG|alt=Com o endereço do Cedente]]