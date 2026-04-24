<!--Foco_2: Modelagem UML Dinâmica.

Entrega Mínima: 1 Modelo Dinâmico (ESCOPO: Diagrama de Sequência; Diagrama de Atividades; Diagrama de Comunicação/Colaboração ou Diagrama de Estados).

Apresentação (para a professora) explicando o modelo dinâmico especificado, com: (i) rastro claro aos membros participantes (MOSTRAR QUADRO DE PARTICIPAÇÕES & COMMITS); (ii) justificativas & senso crítico sobre o modelo, e (iii) comentários gerais sobre o trabalho em equipe. Tempo da Apresentação: +/- 5min. Recomendação: Apresentar diretamente via Wiki ou GitPages do Projeto. Baixar os conteúdos com antecedência, evitando problemas de internet no momento de exposição nas Dinâmicas de Avaliação.

A Wiki ou GitPages do Projeto deve conter um tópico dedicado ao Módulo Modelagem Dinâmica (Notação UML), com 1 modelo, histórico de versões, referências, e demais detalhamentos gerados pela equipe nesse escopo.-->

## 1. Diagrama de Sequência

<iframe width="768" height="432" src="https://miro.com/app/live-embed/uXjVGnju0LM=/?embedMode=view_only_without_ui&moveToViewport=-15481,-1394,3919,1839&embedId=700148791308" frameborder="0" scrolling="no" allow="fullscreen; clipboard-read; clipboard-write" allowfullscreen></iframe>

### Criar Quebra-Cabeças

<p align="center">
    <img src="assets/DiagramaSequencia/DiagramaSequencia1.jpeg" width="100%">
    <figcaption>Diagrama de Sequências. Autores: Fábio Torres, Lucas, Eduardo, Caio, João Felipe</figcaption>
</p>

### Editar dados da conta

<p align="center">
    <img src="assets/DiagramaSequencia/DiagramaSequencia2.jpeg" width="100%">
    <figcaption>Diagrama de Sequências. Autores: Fábio Torres, Lucas, Eduardo, Caio, João Felipe</figcaption>
</p>

### Selecionar quebra-cabeça / Mover peça / Salvar progresso

<p align="center">
    <img src="assets/DiagramaSequencia/DiagramaSequencia3.jpeg" width="100%">
    <figcaption>Diagrama de Sequências. Autores: Fábio Torres, Lucas, Eduardo, Caio, João Felipe</figcaption>
</p>

### Entrar em Partida Online

<p align="center">
    <img src="assets/DiagramaSequencia/DiagramaSequencia4.jpeg" width="100%">
    <figcaption>Diagrama de Sequências. Autores: Fábio Torres, Lucas, Eduardo, Caio, João Felipe</figcaption>
</p>

### Nova Publicação

<p align="center">
    <img src="assets/DiagramaSequencia/DiagramaSequencia5.jpeg" width="100%">
    <figcaption>Diagrama de Sequências. Autores: Fábio Torres, Lucas, Eduardo, Caio, João Felipe</figcaption>
</p>

### Envio de Imagem

<p align="center">
    <img src="assets/DiagramaSequencia/DiagramaSequencia6.jpeg" width="100%">
    <figcaption>Diagrama de Sequências. Autores: Fábio Torres, Lucas, Eduardo, Caio, João Felipe</figcaption>
</p>

## 2. Metodologia
<!--Como fizemos, quando, tem ata? cita aqui, cita referências, pode ser professores etc..-->
Mais uma vez, foi utilizada a ferramenta *online* Miro, e as referências principais foram, por parte das disponibilizadas à disciplina pela profª Serrano, os ***slides* do conteúdo** e a **apostila de UML em português** disponibilizada complementarmente para ele, e, por parte de fontes *online* miscelâneas, alguns vídeos no YouTube da **Bóson Treinamentos**, canal acadêmico/didático sobre tecnologia. Mas, nesse caso, os diagramas foram feitos assincronamente com outra solução *online*, a **Mermaid**, usada como recomendação por causa de um dos próprios vídeos consultados em questão; e então, quando prontos na Mermaid, transferidos para o mural no **Miro** desta própria entrega.

## 3. Justificativa
<!--Falar porque escolhemos fazer esse, porque fizemos assim, mostrar motivos, porque é útil, cita ums fontes, etc... -->
Foi escolhido o **diagrama de sequência** para esta etapa por se mostrar a nós, no cenário geral da Programação Orientada a Objetos, ser uma representação **ideal e poderosa** da interação dinâmica entre objetos no sistema; inclusive, conforme destacado por BARCELAR (2014?), se ressaltando como *sendo* "o diagrama mais utilizado na estapa de Projeto Orientado a Objeto". Permite-se com esse diagrama **modelar o comportamento dinâmico** de ditos objetos, **detalhar casos de uso**, **visualizar o fluxo** de processos, **validar lógica de sistemas do projeto**, **mapear interações** de componentes e **gerenciar o ciclo de vida dos objetos**.

## 4. Senso Crítico
Falar quais conclusões conseguimos tirar desse artefato, satisfez as expectativas do porque é útil?
etc, tem que opinar sobre o artefato.

## 5. Rastreabilidade & Elos com Outros Artefatos

Os Diagramas de Sequência funcionam como o elo comportamental entre o o quê descrito na [Modelagem Organizacional / Casos de Uso](2.3.ModelagemOrganizacionalCasosDeUso.md) e a estrutura definida na [Modelagem Estática](2.1.ModelagemEstatica.md). Cada diagrama abaixo realiza um caso de uso específico do diagrama de Casos de Uso e troca mensagens entre objetos cujos tipos (Controller/Service/Repository e entidades de domínio) derivam diretamente das classes apresentadas no Diagrama de Classes.

A tabela a seguir explicita esse rastro:

| Diagrama de Sequência (2.2) | Caso de Uso realizado em [2.3](2.3.ModelagemOrganizacionalCasosDeUso.md) | Classes manipuladas em [2.1](2.1.ModelagemEstatica.md) |
| -- | -- | -- |
| **DS1 — Criar quebra-cabeça** (`PuzzleController` → `PuzzleService` → `PuzzleRepository` → `Banco`) | *Criar Quebra-Cabeças* (módulo Galeria), incluindo *Obter Imagem* | `QuebraCabeca` (`processarImagem`, `gerarPecas`), `Imagem`, `Peca`, `Usuario` |
| **DS2 — Editar dados da conta** (`ContaController` → `ContaService` → `ContaRepository` → `Banco`) | *Gerenciar Conta* (módulo Jogo, ator externo *Authentication*) | `Usuario`, `Autenticador` (`criarUsuario`, `loginUsuario`, `recuperarSenha`) |
| **DS3 — Selecionar quebra-cabeça / Mover peça / Salvar progresso** (`JogoController` → `JogoService` → `JogoRepository` → `Banco`) | *Jogar Quebra-Cabeça Individualmente* + *Selecionar Quebra-Cabeças para Jogar* + extensão *Salvar Progresso* | `Partida`, `QuebraCabeca` (`iniciar`, `finalizar`), `Peca` (`mover`, `estaMontado`), `Usuario` (`salvarProgresso`) |
| **DS4 — Entrar em partida online** (`OnlineController` → `OnlineService` → `SalaRepository` → `Banco`) | *Jogar Partida 1x1* (atores Usuário e Oponente) | `Partida` com associação `participantes (1..2)` ligando dois `Usuario` |
| **DS5 — Nova publicação** (`PublicacaoController` → `PublicacaoService` → `PublicacaoRepository` → `Banco`) | *Gerenciar Publicações* + extensão *Anexar Conteúdo* (módulo Social) | `Publicação` (`criarPublicacao`, `postarPublicacao`), agregação com `Imagem`, associação com `Usuario` |
| **DS6 — Envio de imagem** (`ImagemController` → `ImagemService` → `ImagemRepository` → `Banco`) | *Obter Imagem* — especialização *Fazer Upload de Imagem* (módulo Galeria) | `Imagem` (`uploadImagem`), associação `ImagensEnviadas`/`ImagensFavoritas` com `Usuario` |

## 6. Comentários sobre o trabalho
...

## 7. Histórico de versões

| Data | Alterações | Autores |
|:----:|------------|:-------:|
| 14/04/2026 | Inserir o template. | Yogi |
| 23/04/2026 | Adicionando imagens dos diagramas de sequência. | Lucas, Fábio Torres, Eduardo, Caio, João Felipe |
| 24/04/2026 | Preenchimento da seção de Rastreabilidade & Elos com Outros Artefatos. | Marcos Vínicius |
| 24/04/2026 | Adicionando metodologia, justificativa e algumas referências. | João Felipe |

## 8. Referências

> DOS REIS, Fábio (BÓSON TREINAMENTOS). **Dica de Ferramenta de Diagramação de Software: Mermaid**. 2022. Disponível em: <<https://youtu.be/5AV6SkaEmqA>>. Acesso em: 23 abr. 2026.

> DOS REIS, Fábio (BÓSON TREINAMENTOS). **Curso de UML - O que é um Diagrama de Sequência**. 2019. Disponível em: <<https://youtu.be/UVkj3ed0ZuM>>. Acesso em: 23 abr. 2026.

> DOS REIS, Fábio (BÓSON TREINAMENTOS). **Curso de UML - Diagrama de Sequência UML - Exemplo Básico**. 2022. Disponível em: <<https://youtu.be/LeV6RO-6Tn4>>. Acesso em: 23 abr. 2026.

> LUCIDCHART. **O que é um diagrama de sequência UML?** Disponível em: <<https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-sequencia-uml>>. Acesso em: 24 abr. 2026.

> BARCELAR, Ricardo R. **- Módulo 3 - Modelagem de Sistemas Orientada a Objetos com UML** (*material complementar da disciplina*). 2014?

> VISUAL PARADIGM. **What is Sequence Diagram?** Disponível em: <<https://www.visual-paradigm.com/guide/uml-unified-modeling-language/what-is-sequence-diagram/>>. Acesso em: 24 abr. 2026.

> IBM. **Rational Software Architect Standard Edition** (Versão 7.5.0). 5 mar. 2021. Disponível em: <<https://www.ibm.com/docs/pt-br/rsas/7.5.0?topic=uml-sequence-diagrams>>. Acesso em: 24 abr. 2026.

> MIRO. **What is a Sequence Diagram in UML?** 5 maio 2025. Disponível em: <<https://miro.com/diagramming/what-is-a-uml-sequence-diagram/>>. Acesso em: 24 abr. 2026.
