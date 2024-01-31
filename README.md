**Teste** : 
#
Para validar os dados cadastrais em um sistema de gerenciamento de usuários, eu criaria os seguintes casos de testes: 
###
*Nome completo*:

1. Testar um nome alfabético válido (João)
2. Testar caracteres especiais válidos (

    Ex: João Paulo de Sousa-Melo

    Ex: D'Angelo Oliveira

)

3. Testar números e caracteres inválidos (

    Ex: João da # Silva

    Ex: João 40 da Silva

)



*Email*:

1. Testar um e-mail válido ( Ex : magazord@magazord.com.br)
2. Testar uma frase sem '@' e sem domínio (Ex: magazord)
3. Testar um e-mail com multiplos arrobas (Ex: magazord@email@magazord.com.br)
4. Testar um e-mail com ponto antes do arroba, no começo ou no final do endereço de e-mail (

    Ex: magazord.@magazord.com.br
    
    Ex: .magazord@magazord.com.br
    
    Ex: magazord@magazord.com.br.
)
5. Testar um e-mail com espaços em branco (

    Ex: magazord@ gmail.com
)
6. Testar # como caracter especial em um e-mail(
    magazord#email@magazord.com.br

)
7. Testar uma frase com apenas arroba e dominio 
(sem nome de usuário, ex: @magazord.com.br)

8. Testar um email com aspas no nome do usuário(Ex: "magazord"@magazord.com.br)

*Número de telefone* :

1. Testar com um número de telefone válido (

    Ex: +55 47 988889900
)

2. Testar com caracteres especiais inválidos (

    Ex : +55 47 @988889900

)

3. Testar com qualquer caracter não número no número de telefone.

*Data de nascimento*:  

1. Testar uma data de nascimento válida (

    Ex: 19/03/2005

)

2. Testar varios formatos de data : ( 

    Ex: DD/MM/AAAA, MM/DD/AAAA, AAAA-MM-DD

)

3. Testar uma data de nascimento passada, do dia atual a uma data anterior ( de preferência com 10 anos passados)

4. Teste com datas muito antigas ( de preferência com o valor máximo de 100 anos passados )

*Endereço* : 

1. Testar com um endereço completo e válido

2. Teste com algum ou todos campos em branco

3. Testar com um CEP válido, que contenha apenas número e o hífen separador (

    Ex: 89160-000

)

4. Testar endereços e CEP's inexistentes

*Combinação dos campos* : 

1. Após todos os testes unitários feitos e correspondidos da forma esperada, realizaria testes em conjunto, para firmar que todos os erros estão filtrados.




**Desafio**: 

Ao analisar o XML a baixo e a imagem disponibilizada neste desafio, cheguei a conclusão que o erro se encontra em:

```
 <referencia>
    <mes>05</mes>
    <ano>2023</ano>
</referencia>
<dataVencimento>2024-01-11</dataVencimento>

```

O erro informado na imagem disponibilizada neste desafio indica que o campo "referencia", filho do campo "item" espera que este campo deve ser o mesmo do vencimento. No XML acima, é possível notar a divergência de valores (referencia do mes 5 de 2023 e o vencimento no mes 01 de 2024). 

```
<?xml version="1.0" encoding="UTF-8"?>
<TLote_GNRE xmlns="http://www.gnre.pe.gov.br" versao="2.00">
    <guias>
        <TDadosGNRE versao="2.00">
            <ufFavorecida>SE</ufFavorecida>
            <tipoGnre>0</tipoGnre>
            <contribuinteEmitente>
                <identificacao>
                    <CNPJ>17637*********</CNPJ>
                </identificacao>
                <razaoSocial>Teste Ltda</razaoSocial>
                <endereco>Rua Emilio Paulo Pilz</endereco>
                <municipio>15802</municipio>
                <uf>SC</uf>
                <cep>89280831</cep>
            </contribuinteEmitente>
            <itensGNRE>
                <item>
                    <receita>100102</receita>
                    <documentoOrigem tipo="10">581</documentoOrigem>
                    <referencia>
                        <mes>05</mes>
                        <ano>2023</ano>
                    </referencia>
                    <dataVencimento>2024-01-11</dataVencimento>
                    <valor tipo="11">491.80</valor>
                    <contribuinteDestinatario>
                        <identificacao>
                            <CNPJ>05578765000127</CNPJ>
                        </identificacao>
                        <razaoSocial>QUALITY BRINDES LTDA</razaoSocial>
                        <municipio>00308</municipio>
                    </contribuinteDestinatario>
                    <camposExtras>
                        <campoExtra>
                            <codigo>77</codigo>
                            <valor>42230517637*********55005000000**1000015949</valor>
                        </campoExtra>
                    </camposExtras>
                </item>
            </itensGNRE>
            <valorGNRE>491.80</valorGNRE>
            <dataPagamento>2024-01-11</dataPagamento>
        </TDadosGNRE>
    </guias>
</TLote_GNRE>
```


