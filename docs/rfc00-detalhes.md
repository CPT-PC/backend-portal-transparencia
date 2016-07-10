---
type: informativo
vers: 0.1
vers_status: RASCUNHO
endorsed_n: 2
endorsed_status: waiting
layout: page
issue: 11
---

&#160; (série "[Request For Comments](https://en.wikipedia.org/wiki/Request_for_Comments) **deste projeto**")

#RFC 00 - Predefinições e modelo de maturidade na informatização da prefeitura

RESUMO: define-se alguns elementos do jargão adotado na RFCs, e um "menu" para posicionamento da prefeitura dentro de uma classificação de tipos de demanda e níveis de maturidade.

[EM DISCUSSÃO E VOTAÇÃO NA *ISSUE*-11](https://github.com/CPT-PC/backend-portal-transparencia/issues/11).

--------

## Terminologia adotada

A adoção de alguns termos e conceitos pressupõe um *modelo de referência* da própria prefeitura. Esse modelo traduz indiretamente as *hipoteses de trabalho* adotadas, e pode se basear em uma visão simples e  pragmática dos municípios e suas demandas.  A seguir os termos principais, adotados na caracterização do grau de informatização das prefeituras.

* Toda prefeitura é composta de **secretarias** (ex. Saúde, Obras e Educação), que é uma espécie de "divisão por assunto". Além delas há algo como o *gabinete*, que faz o papel de "secretaria central".

* Prefeituras maiores podem ser regionalizadas ("divisão espacial"): divididas em distritos e subprefeituras, ou ainda administrações regionais. Podemos adotar o rótulo **subprefeitura** para todas essas denominações.

* Uma prefeitura pode ter boas ideias, bons sites e  boas equipes de suporte e infraestrutura (equipe de TI), ou não.  Rotulemos isso **grau de maturidade informática**. O mesmo vale para a avaliação de partes isoladas da prefeitura, tais como as *secretarias* e *subprefeituras*. A maturidade pode ser classificada como *alta*, *média* ou *baixa*. Opcionalmente "informática madura".

* A mesma equipe e infraestrtura de TI do governo municipal, pode ser suficiente para o tamanho da cidade, ou não. Chamemos a isso de **grau de abrangência da informatização** (grau *alto*, *médio* ou *baixo*). Opcionalmente "informatização agrangente" refere-se a grau alto.

* **ERP** da prefeitura: grandes sistemas de gestão unificados, de apoio à administração  e automação dos processos burocráticos, são em geral designados [ERP (sigla do inglês *Enterprise Resource Planning*)](https://en.wikipedia.org/wiki/Enterprise_resource_planning). Hoje em dia cidades com mais de 200 mil habitantes requerem necessariamente um sistema desse tipo, não se pode gerenciar uma cidade apenas com planilhas.

* **Catálogo** de dados da prefeitura: aplicação Web de catalogação de dados para organização, identificação e publicação de *dados abertos* na forma de arquivos. Referência mais popular, [CKAN](http://docs.ckan.org/). Para conteúdos legislativos e jurídicos o grande catálogo brasileiro é o [LexML](http://www.lexml.gov.br/).

* **Preservação digital**: garantir que os dados continuem existindo, intactos e corretamente identificados, por anos (!) pode ser uma promesssa difícil de se cumprir. Hoje no Brasil o único repositório orientado à transparência e preservação é o [LexML](http://www.lexml.gov.br/), que garante apenas o acervo de metadados e os recursos de identificação de documentos legislativos e jurídicos. Uma das poucas tecnologias para preservação de documentos em seu inteiro teor é a  [LOCKSS](https://en.wikipedia.org/wiki/LOCKSS), utilizado no Brasil pelo SciELO para o acervo de artigos científicos.

### Conceitos alinhados com hipóteses de trabalho

Definidos os termos, resta definir algumas hipóteses (simplificadoras) de trabalho:

* Supondo  que dados são consolidados "por assunto" e pelas secretarias, com o aspecto regional (subprefeituras) subordinado ao assunto (tratado como atributo), pode-se convencionar que  **a secretaria é a autoridade do dado** apresentado num Portal da Transparência.

* Quando não for indicado o contrário, supor que a prefeitura em questão tem *informatização madura e abrangente*.

Tendo esse pequeno jargão descritivo das prefeituras, podemos então falar das decisões racionais que elas tenderiam a tomar.

## Modelo de referência da prefeitura
Todo Portal da Transparência faz parte da infraestrutura de uma prefeitura, a qual, por sua vez, pode ser caracterizada em uma dentre as seguintes possibilidades:

Sistema (ERP)   | Maturidade | Abrangência | Back-end recomendado
--------- | ---------  | ----------- | ----------------
unificado | alta | alta | tipo-1 direto
disperso  | alta | alta | tipo-2 agregador
ausente (‡)  | alta | alta | tipo-3
unificado | média ou baixa | média  | tipo-3
disperso  | média ou baixa | média  | tipo-3
unificado | baixa | baixa | tipo-4
disperso  | média | baixa | tipo-4
ausente  | média ou baixa | média ou baixa | tipo-4

&#160; (‡) apesar de possível em prefeituras maduras, a ausência de ERP só faz sentido em municípios muito pequenos.

* tipo-1: recomenda-se utilizar diretamente o ERP da prefeitura (caracterizado como sistema unificado) diretamente, como *back-end* do Portal da Transparência. Um bom ERP permite ajustes para cumprir normas de publicação de dados, sem demanda por um *middleware* adicional.

* tipo-2: similar ao tipo-1, mas como são diversos "ERPs menores" (p. ex. um por sercretaria), há que se agregar os dados através de um *middleware agregador*, por exemplo fazendo "SQL JOIN" de tabelas recebidas de secretarias diferentes.  

* tipo-3: similar ao tipo-2 mas onde o  *middleware* é um sistema bem mais robusto, que faz conversões e adaptações dos dados, e os mantém de forma definitiva numa base de dados.

* tipo-4: em geral requer apoio humano na consolidação dos dados, e por ser baixa a informatização, não vale a pena (custo e risco) investir num *middleware* de apoio na tarefa. O Portal da Transparência neste caso se resume ao *catalogo* (ex. CKAN) dos arquivos brutos.

Quanto à *preservação digital* dos dados e conteúdos do Portal, trata-se muito mais de contratos e compromissos, do que uma arquitetura: módulos de preservação podem ser imaginados como usuários que acessam e arquivam todos os dados do Portal.

Os três primeiros tipos possuem como referência a [arquitetura de APIs descrita pelo blog da *Open Contracting*](http://www.open-contracting.org/2016/06/30/getting-data-together-routes-towards-ocds-api/).

## Arquitetura do *back-end* direto (tipo-1)
... usando o ERP como *back-end* ... fig1...

## Arquitetura do *back-end* agregador (tipo-2)
... entre o ERP e o Portal tem apenas um pequeno  *middleware agregador* ... fig2...

## Arquitetura do *back-end* completo (tipo-3)
... a arquitetura tem como foco o *middleware* ...  fig3...

## Arquitetura sem *back-end* (tipo-4)
... sugere-se simplesmente fazer bom uso do CKAN ...  fig4...
