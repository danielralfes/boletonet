# Guia do Desenvolvedor

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

Para ajustar a separação entre o símbolo da moeda e o valor **AjustaSeparacaoSimboloMoeda** da classe **BoletoBancário**.

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