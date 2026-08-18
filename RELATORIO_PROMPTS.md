# Relatório de Interação com a IA

## 🤖 IA Utilizada
- **Nome da IA:** Gemini (Google)

## 💬 Prompts Enviados
Abaixo estão os principais prompts enviados para a estruturação do projeto:
1. **Geração do Código:** "Eu preciso criar um jogo da velha para minha cadeira de Requisitos e mod de sistemas, nela eu preciso desenvolver uma atividade Prática: Desenvolvimento Guiado por Requisitos (Spec-Driven Development). Para isso o professor me disponilizou o caso de uso presente na pasta docs.md
2. **Configuração do GitHub:** "Então, preciso subi-lo para o git hub, dessa mesma forma da imagem, como faço ? Me ensine o passo a passo"
3. **Resolução de Erros de Deploy:** Interações sucessivas para resolver questões de inicialização do Git (`git init`), configuração de identidade do autor (`git config`) e ajuste de *case sensitivity* na pasta `/src/` para o correto funcionamento do GitHub Pages.

## ⚠️ Erros da IA e Correções
Em relação ao Caso de Uso (CDU), a IA conseguiu mapear perfeitamente a estrutura solicitada desde a primeira resposta (código em arquivo único HTML, CSS com variáveis da UNIFOR e JS puro com Web Audio API).
- **Correção de Estrutura de Pasta:** A IA orientou a criação da pasta `src`, mas o Windows/Usuário criou com a primeira letra maiúscula (`Src`). Isso gerou um erro 404 no GitHub Pages. A correção foi ordenada navegando até o próprio repositório no GitHub e editando o nome do arquivo/pasta para forçar a nomenclatura `src` (tudo minúsculo), alinhando exatamente à exigência do professor.

## ✅ Autoavaliação dos Critérios de Aceite (CAs)

| Critério de Aceite | Status | Observação / Implementação |
| :--- | :---: | :--- |
| **CA-01 (Fidelidade Visual)** | [X] Atendido | Paleta de cores da UNIFOR aplicada via variáveis CSS (`--unifor-azul`, `--unifor-azul-destaque`) e subtítulo implementado. |
| **CA-02 (Regra de Ocupação)** | [X] Atendido | Validação `options[cellIndex] !== ''` impede sobrescrita no tabuleiro. |
| **CA-03 (Bloqueio pós-Fim de Jogo)** | [X] Atendido | Variável de estado `running = false` bloqueia novos cliques na matriz imediatamente após o fim da rodada. |
| **CA-04 (Comportamento do Modo CPU)** | [X] Atendido | IA da CPU faz a jogada após o intervalo (`setTimeout` de 400ms) quando configurado no seletor de modo. |
| **CA-05 (Regra do Melhor de 3)** | [X] Atendido | Implementado o contador no painel UI-06 e encerramento antecipado caso um jogador atinja 2 vitórias. |
| **CA-06 (Efeitos Visuais de Vitória)** | [X] Atendido | Elemento `win-line` cobrindo a matriz e biblioteca Canvas Confetti importada e funcionando. |
| **CA-07 (Autonomia de Áudio)** | [X] Atendido | Sombras acústicas programadas utilizando `AudioContext` nativo do JS (Oscillators) sem arquivos `.mp3`. |
