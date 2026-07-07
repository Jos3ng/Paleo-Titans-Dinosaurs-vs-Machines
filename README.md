🦖 Paleo Titans: Dinosaurs vs Machines

Um clicker/incremental de navegador onde você reconstitui dinossauros antigos, monta uma equipe elemental e enfrenta um exército infinito de robôs — tudo em um único arquivo HTML, sem instalação, sem build, sem dependências externas.

Abra o paleo-titans.html em qualquer navegador moderno e jogue.


O ciclo principal

Escave fósseis clicando na rocha → incube ovos para descobrir dinossauros → monte uma equipe de até 5 → clique em Iniciar run e deixe a batalha acontecer sozinha, fase após fase, até sua equipe ser derrotada. Perder não é o fim: você mantém coleção, evoluções, itens e relíquias, e ainda ganha DNA ancestral permanente proporcional a quanto essa run avançou além do seu recorde anterior.


Principais sistemas

Escavação


Clique na rocha (agora com um fóssil de verdade — um osso incrustado na pedra, não mais um blob abstrato) para gerar fósseis.
6 melhorias de escavação (pá, picareta, broca, scanner, equipamento automático, laboratório), cada uma comprável individualmente ou com o botão Máx (compra o máximo de níveis que os fósseis atuais permitem).


Coleção — 100 dinossauros


9 elementos: Água, Terra, Pedra, Fogo, Ar, Raio, Luz, Trevas, Nulo — com vantagens e fraquezas elementais (x1.5 / x0.75), Nulo levemente favorecido contra todos.
5 raridades: Comum, Raro, Épico, Lendário, Mítico.
6 classes: Tanque, Guerreiro, Assassino, Mago, Suporte, Curandeiro — cada uma com 3 especializações exclusivas desbloqueadas ao evoluir para Adulto (uma focada em ataque, uma em HP, uma em poder de habilidade).
3 estágios de evolução (Bebê → Adolescente → Adulto), traits aleatórias (Feroz, Resistente, Gênio, Mutante, Lendário) e uma habilidade ativa própria por espécie (cura, escudo, ataque em área, crítico garantido, roubo de vida, congelar, reduzir defesa, entre outras) — os números reais de cada habilidade aparecem na própria aba Coleção.
Corpo e dieta de cada uma das 100 espécies foram curados manualmente pela paleontologia real (nada de Gallimimus virar "aquático" por acaso de um índice) — bípedes, quadrúpedes, voadores e aquáticos com silhuetas e posturas anatomicamente coerentes.


Equipe e sinergias

Até 5 dinossauros ativos, com bônus de composição:


Monoelemental, Diversificada, 2 Fogo+2 Raio, 2 Água+2 Terra, 2 Luz+2 Trevas, 2 Pedra+2 Terra
Manada Herbívora, Alcateia Carnívora, Esquadrão Alado, Cardume Predador (times completos de herbívoros, carnívoros, voadores ou aquáticos)
Itens do tipo "Cristal de Afinidade" concedem um elemento secundário a um dinossauro, somando-o às sinergias sem remover o elemento original.


Itens

Chefes robóticos têm chance de dropar equipamentos (armas, armaduras, reatores, sensores, amuletos). Cada dinossauro equipa apenas 1 item por vez. Itens no inventário podem ser vendidos individualmente ou em lote por raridade, com confirmação de segurança ao vender itens Lendários/Míticos.

Batalha


Modo totalmente automático: iniciar uma run encadeia as lutas sozinho até a derrota — sem espaço para farmar indefinidamente entre estágios.
6 tipos de robôs com silhuetas próprias (Drone, Tanque, Androide, Mecha, Torre de Defesa, Chefe Robótico), escalando infinitamente em dificuldade.
Feedback visual de combate: partículas de cura, escudo, crítico, projéteis elementais (temáticos por elemento) e efeitos de todas as habilidades ativas, desenhados em tempo real no canvas.
Efeitos sonoros sintetizados via Web Audio API (escavação, ataques) — sem nenhum arquivo de áudio externo.


Prestígio, DNA e Relíquias

Cada derrota concede DNA ancestral automaticamente, calculado sobre o quanto a run avançou além do seu recorde pessoal anterior — repetir uma run sem progresso genuíno não rende nada. O DNA é investido em Relíquias: melhorias permanentes de produção, experiência, sorte, dano e HP.

Missões e progressão de longo prazo


Missões diárias: 3 desafios rotativos que se renovam a cada dia real.
Marcos de progresso: 6 trilhas permanentes (coleção, robôs derrotados, chefes, ovos incubados, evoluções, fase alcançada), cada uma com vários degraus e recompensas crescentes.
Conquistas clássicas de marco único.


Onboarding


Tutorial guiado passo a passo para novos jogadores: destaca um elemento real da interface por vez (nada de popup com parede de texto), com "Pular tutorial" sempre disponível e sem nenhum ponto de travamento possível.
Guia de referência completo (botão ❓), dividido em seções — sinergias e prestígio, sendo os tópicos mais complexos, têm seção própria e detalhada.



Tecnologia

Um único arquivo .html autocontido: HTML + CSS + JavaScript puro, sem frameworks, sem build step, sem requisições de rede em tempo de jogo.


Renderização: todo o elenco de dinossauros e robôs é desenhado proceduralmente via Canvas 2D (nenhuma imagem/sprite externa).
Áudio: sintetizado via Web Audio API.
Persistência: localStorage, com exportação de save em base64 e opção de reset completo.
Save: compatível com versões anteriores — saves antigos são migrados automaticamente ao carregar.



Rodando localmente

Não precisa de nada além de um navegador:

bash# clone o repositório e abra o arquivo direto
open paleo-titans.html   # macOS
start paleo-titans.html  # Windows
xdg-open paleo-titans.html  # Linux

Ou simplesmente dê duplo clique no arquivo.


Changelog resumido desde a primeira versão


Reescrita completa do sistema de habilidades ativas com números reais visíveis na UI
Sistema de itens com equipamento único por dinossauro, drop exclusivo de chefes e venda
18 especializações de classe (3 por classe) substituindo o sistema genérico original
Modo de batalha totalmente automático (run começa e encadeia sozinha até a derrota)
DNA ancestral automático ao perder, escalado pela melhora sobre o recorde pessoal
Sistema de missões diárias rotativas + marcos de progresso em camadas (substituindo as 5 missões fixas originais)
Redesenho completo da arte procedural: posturas de dinossauros corrigidas para o padrão paleontológico atual, corpo/dieta de cada espécie curados manualmente, 6 robôs com silhuetas distintas
Feedback visual de combate (partículas por habilidade) e efeitos sonoros sintetizados
Botão de escavação redesenhado (fóssil incrustado em rocha)
Tutorial guiado interativo + guia de referência sectionado
Diversas correções de qualidade de vida (comprar máximo, incubar em lote, venda em lote, desequipar rápido) e de balanceamento (remoção de brechas de farm infinito)
