Case: requisitos da prefeitura de São Paulo

Recomendações técnicas para o back-end do "Portal de Transparência" da capital de SP


## Links externos

* separata do DOM-SP, "AVISO DE AUDIÊNCIA PÚBLICA PARA APRESENTAÇÃO E ESCLARECIMENTOS SOBRE A LICITAÇÃO PARA A REFORMULAÇÃO DO PORTAL DA TRANSPARÊNCIA", [Diário-Livre de Sampa 2016/05/01/149](http://devcolab.each.usp.br/do/2016/05/01/149)
  * Inscrições pelo formulário http://goo.gl/forms/l8LK6COm7c (com outros links e explicações)

* "CONSULTA PÚBLICA: NOVO PORTAL DA TRANSPARÊNCIA, Instruções", [saopauloaberta.prefeitura.sp.gov.br]( http://saopauloaberta.prefeitura.sp.gov.br/index.php/minuta/consulta-publica-novo-portal-da-transparencia/)

* [Diretrizes tecnológicas para o portal de transparência do município de São Paulo](https://docs.google.com/document/d/1EYWfgk-BqCoXD4OFpLSD9aOMe2bog7EtBLnfsx0VuJ4/edit), GDoc do USP/COLAB.

* Diário Oficial da Cidade de São Paulo sábado, 18 de junho de 2016, pag. 154

------
Transcrição do [DOM-SP contendo a ata](http://www.docidadesp.imprensaoficial.com.br/RenderizadorPDF.aspx?ClipID=2M6239RR2LKA4e2IU4MOJVDPFN0), 

## ATA DE AUDIÊNCIA PÚBLICA

Ata da Audiência Pública para a reformulação do Portal da
Transparência. Ao dia treze do mês de maio de dois mil e dezesseis
(13/05/2016), às dez horas e dezessete minutos (10h17), no
auditório do 8º andar da Galeria Olido, realizou-se a audiência
pública para discutir a reformulação do Portal da Transparência,
organizada pela Coordenadoria de Promoção da Integridade
(COPI) da Controladoria Geral do Município (CGM).

A audiência foi iniciada por Fernanda Campagnucci, Coordenadora
de Promoção da Integridade, que explicitou os objetivos
deste encontro técnico, quais foram: i) levantar aspectos
do mercado de tecnologia e, para tanto, o convite foi estendido
às pessoas físicas e jurídicas interessadas no desenvolvimento
desse projeto; ii) esclarecer detalhes sobre as principais ferramentas
e especificações técnicas que constarão na licitação da
plataforma.

Além disso, Fernanda especificou que o processo de reformulação
do Portal da Transparência contou com etapas
participativas, por meio de consulta pública e do Café Hacker
realizados no mês de abril desse ano, que buscaram levantar as
principais demandas e funcionalidades do Portal. Nesse sentido,
ponderou que a audiência pública cumpria a função de discutir
as ferramentas e especificidades tecnológicas a constar nos
documentos licitatórios.

Depois de relatar os objetivos do encontro, Fernanda fez
a apresentação sobre os principais aspectos do atual Portal da
Transparência e as demandas solicitadas pela Controladoria
Geral do Município para reformulação da plataforma. A apresentação
se encontra a disposição para consulta na página web  http://bit.ly/Apresentação_Portal .

Antes de abrir para o debate, Fernanda ainda levantou
questões que estão a serem definidas, como dimensionamento

presa que estruturou um Portal da Transparência para conselho
regional, disse que o back end deve ser estruturado para raspar
dados e fornecê-los e, por fim, que 6 meses é pouco tendo em
vista a complexidade do projeto.

Vinicius disse que a divisão posta em módulos é complicada
pelo nível de maturidade do processo licitatório. Julga
importante realizar uma licitação específica para que empresa
desenhe escopo, detalhamento das fontes e projetos para, então,
pautar o desenvolvimento da ferramenta.

Fernanda interveio para perguntar se o planejamento
exaustivo por um empresa é um modelo viável ou se o planejamento
na medida em que se desenvolve é uma boa saída.
Ademais, perguntou qual o tempo exequível, uma vez que os
participantes apontaram os 6 meses como inviáveis.

Vinicius avaliou que a proposta apresentada é diferente
da SCRAN, mas é uma maneira de mitigar os riscos e ser mais
garantida, do ponto de vista do planejamento e da entrega, a
adoção de um modelo de planejamento prévio por empresa
específica. Gabriel complementou que o problema do prazo
está, justamente, no levantamento das informações e fontes
necessárias.

Peter relatou que a maior dificuldade nesses processos é a
obtenção e levantamento de dados confiáveis. Daniel agregou
ainda que o prazo é limitador pelo risco dos sistemas em fornecer
dados. Fernanda respondeu que existem fontes seguras para
obtenção dos dados e a maior dificuldade seria na obtenção
dos dados de compras públicas, uma vez que seriam extraídos,
no pior cenário, do Diário Oficial. Reforçou, ainda, que uma API
facilitaria a extração desses dados.

Diego reforçou que, adotada a estratégia de separação
entre Back end e Front end, deve haver um documento prévio
definindo o escopo de trabalho de cada empresa. Ainda sim,
retomou a discussão sobre aplicativos enfatizando que os mesmos
valorizam o projeto e que o limitador, nesse caso, seria o
tempo. No curto prazo, um portal responsivo resolveria a questão.
No médio e longo prazo, um aplicativo seria ideal. Gabriel
complementou que o aplicativo proverá respostas rápidas se
tiver acesso rápido os dados.

Simon reforçou que é importante escolher um módulo com
uma fonte de dados confiável para o primeiro desenvolvimento.
O desenvolvimento de vários módulos simultâneos imputa
vários riscos ao projeto.

De modo geral, os participantes discutiram sobre a necessidade
de se estabelecer CMS anterior e sobre o processo de
licitação. A abordagem SCRAN, nesse sentido, permite testar
uma ferramenta e remodular pensando no produto final.
Peter comentou que é importante haver padronização e
possibilidade de contribuição do público. Perguntou, ainda,
como se dará o processo de desenvolvimento colaborativo.
Fernanda respondeu que foram apresentados os módulos,
mas que nem todos são complexos. Alguns preveem consultas
simples com nível de dificuldade baixo. Ainda, questionada sobre
a possibilidade de se fazer uma hackatona, respondeu que
houve um processo de Café Hacker para o módulo de compras
abertas, mas o desenvolvimento por empresa é necessário para
estruturação da ferramenta.

Andrés concordou com a avaliação e disse que um Back
end único não seja tão ideal, mas sim vários back end para
cada módulo, fornecendo APIs. Peter completou que com o
código fonte aberto a colaboração é maior e que, portanto,
a equipe é não convencional. Levantou, ainda, a necessidade
de haver duas licitações: uma de back end para módulos mais
complexos e outra para agregar os dados do Diário Oficial.

Fábio perguntou se os seis meses apresentados considera a
relação funcional com a PRODAM, considerando o fato de que
será necessário tratar dados e implantar o sistema. Pontuou
que não deve haver separação entre os módulos, mas sim um
projeto integral, como um todo. Para tanto, acha importante
aumentar a equipe demandada.

Fernanda reiterou que os detalhes técnicos estão em discussão
e que a COPI não definiu previamente todos os pormenores
do processo. Ademais, colocou que a modalidade
de licitação está em aberto e que a PRODAM entraria como
figura contratual de interventora para validar e incorporar as
ferramentas desenvolvidas. Esse processo prevê a incorporação
das ferramentas durante o processo e não ao fim, modelo que
trará a PRODAM presente no processo. Fernanda ainda relatou
que a PRODAM já hospeda os dados, mas ponderou se seria
necessário hospedar o Portal dentro da Empresa Municipal,
uma vez que a plataforma funciona como aplicação dos dados
disponíveis. Levantou, ainda, se é possível prever um contrato
específico para serviço de hospedagem.

Andrés reforçou que se o acesso aos dados hospedados em
servidores da Prefeitura for facilitado, a hospedagem da Plataforma
pode ser fora. Ainda questionou como funcionaria esse
processo. Peter reforçou que é possível hospedar o Portal fora.
Gabriel, por fim, que a hospedagem externa pode funcionar e a
PRODAM seria um repositório de back up. Para isso, a manuten-
ção seria em um contrato a parte.
Nada mais havendo para tratar, Fernanda declarou encerrada
a audiência às doze horas e nove minutos (12h09).
A lista dos presentes na audiência sobre a reformulação do
Portal da Transparência encontra-se abaixo.

|Nome|Email|Entidade|
|----|-----|--------|
Andrés M. R. Martano|andres@inventati.org|Digital Ikotema
Daniel Doglas Silva|daniel@madeinweb.com.br|MadeinWeb e mobile
Diego Rabatone Oliveira|diego@ask.ar.com; diraol@diraol.eng.br|ASk-AR
Fábio Pulitta|fabio@camaleoa.com|Camaleoa
Gabriel Henrique Dias|dias@himaker.com.br|Himaker Sistemas Ltda
Gioia Matilde Alba Tumbiolo Tosi|gioiatt@yahoo.com.br|Observatorio Social
Leonardo Zanon Arruda|lzanon@prefeitura.sp.gov.br|Controladoria Geral
Neusa Romano|neusar@hotmail.com; neusa@camaleoa.com|Camaleoa
Peter Krauss|ppkrauss@gmail.com|COLAB-USP
Ronaldo Cancian|rcancian@prefeitura.sp.gov.br|CGM
Simon Fan|simonxd@gmail.com|Habemus
Thiago Fassoni A. A. Leite|tiago@openstreetmap.com.br|Fundação OpenStreetMap
Thiago Rondon|thiago@appcivico.com|App Civico
Vinicius Gallafrio|vgallafrio@madeinweb.com.br|MadeinWeb e Mobile




