<!--Foco_2: Modelagem UML Dinâmica.

Entrega Mínima: 1 Modelo Dinâmico (ESCOPO: Diagrama de Sequência; Diagrama de Atividades; Diagrama de Comunicação/Colaboração ou Diagrama de Estados).

Apresentação (para a professora) explicando o modelo dinâmico especificado, com: (i) rastro claro aos membros participantes (MOSTRAR QUADRO DE PARTICIPAÇÕES & COMMITS); (ii) justificativas & senso crítico sobre o modelo, e (iii) comentários gerais sobre o trabalho em equipe. Tempo da Apresentação: +/- 5min. Recomendação: Apresentar diretamente via Wiki ou GitPages do Projeto. Baixar os conteúdos com antecedência, evitando problemas de internet no momento de exposição nas Dinâmicas de Avaliação.

A Wiki ou GitPages do Projeto deve conter um tópico dedicado ao Módulo Modelagem Dinâmica (Notação UML), com 1 modelo, histórico de versões, referências, e demais detalhamentos gerados pela equipe nesse escopo.-->

## 1. Diagrama de Estados

### Estados do Jogo 

<p align="center">
    <img src="assets/diagrama-estados/Jogo.png" width="50%">
    <figcaption>Diagrama de Estados. Autores: Yogi, Carlos, Pedro </figcaption>
</p>

### Estados do Partida 1x1

<p align="center">
    <img src="assets/diagrama-estados/1x1.png" width="50%">
    <figcaption>Diagrama de Estados. Autores: Yogi, Carlos, Pedro  </figcaption>
</p>

### Estados Publicação

<p align="center">
    <img src="assets/diagrama-estados/publi.png" width="30%">
    <figcaption>Diagrama de Estados. Autores: Yogi, Carlos, Pedro  </figcaption>
</p>

### Estados Conquistas

<p align="center">
    <img src="assets/diagrama-estados/conquistas.png" width="50%">
    <figcaption>Diagrama de Estados. Autores: Yogi, Carlos, Pedro  </figcaption>
</p>

## 2. Metodologia
<!--Como fizemos, quando, tem ata? cita aqui, cita referências, pode ser professores etc..-->
Realizamos discussões assíncronas pelo Whatsapp [Discussão](Discussoes/estados.md) e fizemos uma reunião com parte do grupo [Ata](AtasReunioes/Ata3.md). A modelagem foi conduzida com foco no ciclo de vida das entidades de maior complexidade identificadas previamente no Diagrama de Classes. Aplicamos uma análise orientada a eventos, mapeando transições a partir das interações do usuário com a interface e das regras de negócio de retaguarda. Os fluxos foram extraídos dos requisitos de jogabilidade, sincronização multiplayer e interações sociais, definindo os estados, condições de guarda e os gatilhos (triggers) que alteram o comportamento do sistema. Usamos como base as descrições em [uml-diagrams](https://www.uml-diagrams.org/state-machine-diagrams.html)

## 3. Justificativa
<!--Falar porque escolhemos fazer esse, porque fizemos assim, mostrar motivos, porque é útil, cita ums fontes, etc... -->
Enquanto o diagrama de classes estabelece a estrutura estática, ele é ineficaz para demonstrar mutações temporais. O uso de diagramas de máquina de estados é mandatório para documentar o rigor da lógica de controle interno, especialmente em fluxos críticos como a concorrência de uma partida 1x1, as físicas de manipulação de peças e as transições de publicação de mídia. Esses artefatos fornecem a base exata e inambígua necessária para a implementação dos gerenciadores de estado no código-fonte.

## 4. Senso Crítico
Os diagramas elaborados são diretos e cobrem adequadamente as mudanças de estado exigidas pelas regras de negócio. Servem como um roteiro estrito para prevenir estados fantasmas na codificação. No entanto, assim como outros diagramas é difícil mapear todos os estados, pois situações de erros podem ocorrer em diversas fases, levando a varias situações de exceção. Mas fora isso, é um ótimo diagrama para representar os módulos do nosso projeto, porque a maioria das funcionalidades não é exatamente linear, acabam tendo loops que é bem representado nesse tipo de diagrama.

## 5. Rastreabilidade & Elos com Outros Artefatos
| Entidade Modelada | Classe Relacionada | Caso de Uso Correspondente |
|:----:|------------|:-------:|
| Partida Multiplayer (1x1) | Partida, Usuario | Jogar Partida 1x1 |
| Sistema de Conquistas | Usuario | Visualizar Estatísticas e Conquistas |
| Quebra-Cabeça | QuebraCabeca, Peca | Jogar Quebra-Cabeça Individualmente |
| Galeria e Publicações | Imagem, Publicacao | Gerenciar Publicações, Gerenciar Favoritos |

## 6. Comentários sobre o trabalho
...

## 7. Histórico de versões

| Data | Alterações | Autores |
|:----:|------------|:-------:|
| 24/04/2026 | Primeira versão do diagrama de estados. | Yogi |
| 24/04/2026 | Adição de metodologia, justificativa, senso crítico, e rastreabilidade. | Yogi, Carlos, Pedro |

## 8. Referências

> UML DIAGRAMS. State Machine Diagrams. [S. l.], 2024. Disponível em: https://www.uml-diagrams.org/state-machine-diagrams.html. 

> LUCIDCHART. O que é diagrama de máquina de estados UML? [S. l.], 2024. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-maquina-de-estados-uml.
