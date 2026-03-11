# 🌵 Inanna — Proto-IA Educativa (Cordel 2.0)

Laboratório de compreensão da Inteligência Artificial. 
Inanna Proto-IA é um aplicativo educativo interativo que simula de forma transparente como sistemas de Inteligência Artificial preveem a próxima palavra em um texto. O app permite que usuários escrevam o início de um verso e observem como uma proto-IA pedagógica sugere possíveis continuidades com probabilidades associadas.

A experiência combina:
- Criatividade literária
- Cultura do Cordel
- Aprendizado sobre modelos de linguagem
- Compreensão crítica da Inteligência Artificial

O projeto é também uma homenagem à Inanna, uma gatinha siamesa adotada da rua, símbolo da união entre afeto, cuidado e tecnologia educativa. Ao longo do jogo, Inanna interage com o jogador por meio de avatares carismáticos em visualação estilo Roblox.

## 🎯 Objetivo Pedagógico

O aplicativo foi criado para ensinar como funcionam os modelos de linguagem (como os usados em IA generativa) de maneira acessível. Ele demonstra conceitos fundamentais:
- Previsão de próxima palavra (token)
- Probabilidade linguística
- Escolha entre alternativas possíveis
- Diferença entre criatividade humana e previsão algorítmica

**A Inanna não é uma IA real.** Ela é uma *proto-IA* pedagógica que permite visualizar os princípios básicos da tecnologia.

### Público-alvo (12 anos ou mais)
- Escolas e Universidades
- Oficinas de tecnologia e Laboratórios de escrita criativa
- Cursos de letramento digital
- Introdução à Inteligência Artificial

## ⚙️ Como Funciona o Jogo

O fluxo do aplicativo simula o uso de modelos de linguagem:

1. **Escolha de Contexto (Tema):** O jogador define o "Corpus" inicial, com temas variados que vão de *Nordeste* e *Festa Junina* até *Shopping* e *Tecnologia*.
2. **Entrada de Texto:** O usuário escreve o início de um verso usando uma lacuna (`___`). (Ex: "No sertão eu vi a ___")
3. **Predição e Escolha:** A Inanna aciona sua engine de probabilidade simulada e sugere continuações, separando rigorosamente listas de *substantivos*, *adjetivos* e *verbos*, e oferecendo também a possibilidade de o jogador inventar sua própria palavra (superando a máquina).
4. **Construção e Placar:** Ao finalizar uma quadra (4 versos), o jogador envia sua obra. 

### Modos de Jogo:
- **Modo Didático:** O foco é explorar e aprender tranquilamente como a rede monta os textos contextuais.
- **Modo Desafio:** O jogador interage com o Placar em Destaque. Ganha 1 ponto sempre que conseguir construir uma frase em que a IA preveja opções com Confiança Baixa (< 42%), recompensando a fuga do óbvio. Os melhores textos submetidos formam um ranking online!

## 🚀 Tecnologias Utilizadas e Integração

O frontend é flexível e projetado para fácil uso em instituições educacionais:
- **HTML, CSS (Vanilla) e Javascript**
- **Github Pages** para hospedagem estática direta.

O backend e banco de dados é gerido via:
- **Google Apps Script & Google Sheets:** Todas as submissões de quadras e exibição de placares são transferidas diretamente para uma planilha na nuvem via API RESTful simples (`/doPost` e `/doGet`). Este formato dispensa servidores pesados, não contém problemas de CORS Preflight perigosos graças à transmissão limpa, e armazena até os modos de partida.

### Estrutura do projeto

```text
inanna-main/
├── index.html         # Template principal da aplicação com as Etapas do Jogo
├── styles.css         # UI moderna, responsiva, glassmorphism e animações 2D/3D (float)
├── app.js             # Motor da Proto-IA, estado do jogo, Modais e Fetch Actions
├── apps_script.gs     # Lógica Back-End do Google Apps Script
├── cat_*.png          # Gatinhas Siamesas Estilo Roblox e demais assets de UI
└── README.md          # Documentação do projeto
```

## 🛠️ Como Executar Localmente

Você pode simplesmente abrir o arquivo `index.html` em qualquer navegador, e o projeto funcionará com dados pré-programados (*Mock Data/Library*) até estabelecer uma rede ao Google Apps. 

Para rodar de forma perfeitamente em torno de uma visualização host, inicie um servidor web local em sua pasta.
```bash
# Via Node.js (npx)
npx http-server ./ -p 8080

# OU Via Python
python -m http.server 8080
```
E acesse `http://localhost:8080` de seu navegador.

## 📜 Licença e Direitos Autorais

**"Inanna e Cordel 2.0" by Celeste Farias e Carlos Vidal é protegido por direitos de autor sob CC BY-ND 4.0.**

Este aplicativo faz parte do ecossistema educativo do **Projeto Cordel 2.0** — dedicado a explorar relações entre cultura popular, criatividade, educação e tecnologias emergentes.
