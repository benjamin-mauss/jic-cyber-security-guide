# Guia de estudos para Web Hacking \[2021\]
![WEBHACKING](https://user-images.githubusercontent.com/86640585/137555285-2818548d-68f9-4658-b248-c3776367303a.png)

## Apresentação

O projeto surgiu quando os integrantes do grupo perceberam que a demanda por profissionais de segurança da informação está cada vez maior e há uma falta enorme de profissionais qualificados. Os conteúdos dispersos confundem estudantes que querem aprender ou, muitas vezes, por ser um ramo novo, há um desconhecimento da área.

Somente em 2021, ataques hackers já atingiram US$ 6 trilhões em prejuízos, dinheiro que poderia estar sendo investido em avanços tecnológicos, segurança ou educação. Ataques hackers a hospitais, usinas nucleares e grandes estruturas podem acabar em tragédias, gerando perda de vidas.

O objetivo deste projeto é orientar o que os estudantes interessados em web hacking devem aprender, afim de ajudar a mitigar a falta desses profissionais no mercado.

O método empregado é criação de um website que faz a indexação de materiais didáticos, gratúitos e de qualidade sobre web hacking, o qual os estudantes usarão como um guia em seus estudos de segurança da informação, sendo eles materiais em inglês e em português.

O estudante e autor deste projeto, Benjamin Walter, segue esta metodologia. Atualmente ele trabalha na área de segurança de informação, encontrando e reportando, eticamente, vulnerabilidades para grandes empresas como Facebook, Shopify, Mercado Livre, CS Money, Avast, Google, Discord e outros programas de recompesas por vulnerabilidades privados.




## Tabela de conteúdos
- [Apresentação](#apresentação)
- [Tabela de conteúdos](#tabela-de-conteúdos)
- [Introdução](#introdução)
  - [O que é web hacking?](#o-que-é-web-hacking)
  - [Por quer ser um web hacker?](#por-quer-ser-um-web-hacker)
- [O inglês é essencial!](#o-inglês-é-essencial)
- [O que você precisa saber antes de começar no web hacking?](#o-que-você-precisa-saber-antes-de-começar-no-web-hacking)
  - [Lógica de programação](#lógica-de-programação)
  - [OAC - Organização e arquitetura de computadores](#OAC---Organização-e-arquitetura-de-computadores)
  - [C/C++](#)
  <!-- Devo incluir assembly? Acho que não, pois é web. OAC já vai dar -->
  - [HTML - HyperText Markup Language](#)
  - [CSS - Cascading Style Sheets](#)
  - [Javascript](#)
  - [PHP - Hypertext Preprocessor](#)
  - [MySQL](#)
  - [Redes](#) 
    - [Protocolo TCP/IP](#)
    - [Protocolo HTTP](#)
    - [Protocolo UDP](#)
  - [Linux](#)
  - ...
- [Vulnerabilidades](#)
  - [DOS](#)
  - [SQL Injection](#)
  - [XSS](#)
  - [CSRF](#)
  - [IDOR](#)
  - ...
- [Reconhecimento do alvo](#)
  - [Enumeração de subdomínos](#)
  - [Enumeração de portas](#)
  - [Google dork](#)
  - [Crawling](#)
- [Ferramentas](#)
  - [Sqlmap](#)
  - [amass](#)
  - [nmap](#)
- [Bug bounty](#)
  - [Como participar](#)
  - [Plataformas](#)
- [CTF](#)
  - [Como participar](#)
  - [Plataformas](#)
- [Pentest](#)
  - [Como começar no pentest](#)
  - [Certificações](#)
- [License](#license)
- [Fontes](#fontes)

## Introdução

### O que é web hacking?

Web Hacking são as atividades que procuram comprometer websites, seja obtendo controle completo sobre o website, vazando informações confidenciais ou tornar os  recursos do alvo indisponíveis (Ataque de negação de serviços).

### Ser hacker é ser criminoso?

Ao contrário do que muitos pensam, ser hacker não é ser criminoso. É verdade, muitos hackers usam seu conhecimento para o mal, afim de tirar vantagens para si mesmo. Porém, neste projeto, estaremos abordando somente o hacking ético, o tipo que você tem permissão para hackear.

### Por que ser um hacker?

#### Curiosidade

Essa é, provavelmente, a porta de entrada para o mundo dos hackers: um desejo quase incontrolável de investigar, de entender algo. Durante a infância, muitos quebravam os próprios brinquedos, apenas para descobrir como eles funcionavam. Desmontavam partes, encaixavam com pedaços de outros brinquedos, modificavam, criavam algo novo.

No mundo dos computadores, isso funciona da mesma forma. É a curiosidade que move o hacker a entender como um software é construído. Com isso, eles aprendem a programar, estudando linguagens de programação e construindo seus próprios programas. Melhor ainda, eles adquirem um conhecimento muito mais amplo do funcionamento de um programa de computador, possibilitando a exploração de falhas e bugs.

Muitas vezes essa também é a motivação para a invasão de sistemas online: apenas conferir como isso é possível, descobrir quais são os passos necessários.

#### Diversão

Outro fator que conta muito para o hacker é a diversão. Antes de qualquer coisa, o hacker tem que gostar do que está fazendo e se divertir com aquilo. Caso contrário, ele não se dedicará tanto quanto gostaria.

#### Desafio

O hacker precisa se sentir desafiado, instigado a prosseguir com a ação. Muitas vezes essas pessoas agem somente por agir, para perceberem que algo é possível e que eles conseguem fazer. Hackers gostam de resolver problemas e, quanto mais complexos esses problemas, melhor. Diga a um hacker que algo é impossível de ser feito e ele vai tentar até conseguir.

#### Liberdade

Hackers gostam de explorar os limites de tecnologias e equipamentos e não querem ficar limitados ao uso imposto pela indústria ou fabricante de um dispositivo.

#### Dinheiro

Trabalhar como pentester ou bug bounty hunter pode gerar uma grana legal. Fazer uma empresa que realiza pentest pode ser um negócio muito lucrativo.
Muitas vezes, um pentest que dura poucos dias, pode ser cobrado valores maiores que USD $50,000.00, mas claro, para isso você tem que ser bom, ter certificações e experiência na área. Bug bounty hunter é algo super lucrativo também: as empresas pagam em dólar, valores que variam entre $50 e $50k, dependendo da vulnerabilidade e da empresa em que foi encontrada a falha.

### Por que uma empresa contrataria um hacker?

Uma falha de segurança pode ser catastrófica para uma empresa. 
Uma empresa só abre bug bounty público/privado quando tem certeza de que não consegue encontrar nenhuma vulnerabilidade em seu sistema, depois de pagar por pentester e ter analistas de segurança da informação analizando os códigos.
O pentest ocorre antes do bug bounty. As empresas pagam para que pentester testem a aplicação delas, à procura de vulnerabilidades.

### Você não precisa ser um gênio para aprender hacking

Real. Demora, exige dedicação, às vezes você não entende o que o instrutor está falando e tem que pesquisar sobre um assunto, então descobre que tem ainda mais para aprender.

## O inglês é essencial!

99% dos conteúdos estão em ingles. Não há como fugir. Seus reportes \[de vulnerabilidades\] serão, em suma, todos em inglês. Você não precisa ser fluente, mas um inglês tecnico dá conta legal. Se tu conseguir ler livros em ingles, melhor ainda.

Tem um podcast que eu gosto muito, é o [Inglês do Zero](https://podcasts.google.com/feed/aHR0cHM6Ly9mZWVkcy5zb3VuZGNsb3VkLmNvbS91c2Vycy9zb3VuZGNsb3VkOnVzZXJzOjMzNzMxMDg5My9zb3VuZHMucnNz/episode/dGFnOnNvdW5kY2xvdWQsMjAxMDp0cmFja3MvMTE0MjIzNDA1OQ)
Você também pode fazer um curso online gratúito. Inglês não é algo difícil de aprender, com o tempo você pega. Ouça música e veja análises de músicas em ingles. 
Veja vídeos do youtube em inglês \[são muito bons\]
Use o google translator sempre que necessário, não é vergonha nenhuma, ninguém é um dicionário.

## Participe de comunidades de cyber segurança

Discord.
Se você ainda não conhece essa plataforma (estilo rede social), está perdendo.
Você pode criar uma conta e participar de servidores focados em ethical hacking, sejam eles portugues ou ingles.
- (Boitatech)[https://www.boitatech.com.br/] Gurizada BR de hacking, bem interessante. \[pt\]
- (Public club)[https://discord.gg/2EDuJR3c4K] Tudo que é tipo de hacking ou assunto de tecnologia. Tem bastante gente crânio nesse server. \[en\]
- (Intigriti)[https://discord.gg/vdFTaHgz2d] Web Hacking, tutoriais bons \[en\]
- (Hackerone)[https://discord.gg/Qqfwmfuav7] Web Hacking, tutoriais bons \[en\]
- (XSS Rat)[https://discord.gg/2EDuJR3c4K] Web Hacking e instruções para iniciantes \[en\]
- (InsiderPHP)[https://discord.gg/2sFmxQwg4e] Web Hacking e instruções para iniciantes \[en\]
- (Mente Binária)[https://menteb.in/discord] Mais focado em low level hacking, mas tem web hacking tbm \[pt\]



## Ebooks e livros que vão te ajudar

- Ebook grátis da [hackerone] (https://www.hackerone.com/ethical-hacker/hack-learn-earn-free-e-book): 
- Bug Bounty Bootcamp by Vickie Li
- Bug Hunter Diary
- Hands-On Bug Hunting for Penetration Testers 1st Edition
- The Web Application Hacker's Handbook [Este é realmente muito bom]

## Onde se informar sobre novas vulnerabilidades e se manter atualizado
- Hackctivity da hackerone, bugcrowd, YesWeHack, etc., todas essas plataformasde reportes de vulnerabilidades
- Artigos no medium.com. Tente procurar pelas tags `hacking`, `hackerone`, `cybersec`.
- Twitter. Pode parece meio plot twist, mas o twitter é uma fonte de informação muito boa quando se diz respeito à tecnologia. Muitas vulnerabilidades 0days são compartilhadas lá. Recomendo a criação de uma conta onde você fique cercado nesse universo da cybersec.
- O youtube tem vários hackers muito bons também. Algumas lives lhe ajudarão bastante

## Fontes

- [Hacker roadmap](https://github.com/sundowndev/hacker-roadmap)
- [Dados de ataques hackers](https://olhardigital.com.br/2021/09/12/seguranca/brasil-e-o-5o-pais-em-ataques-de-hackers-contra-empresas)
- [hacker](https://br.malwarebytes.com/hacker/)
- [razões para hackear](https://www.tecmundo.com.br/seguranca/10731-7-razoes-para-hackear.htm)
