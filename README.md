# 🏨 Sistema de Orçamentos

Um gerador e gerenciador de orçamentos para reservas de grupos em hotéis e hostels. A aplicação foi projetada para otimizar o atendimento via WhatsApp, automatizando cálculos de estadias e extração de dados através de um arquivo local único (Single-file).

## 🚀 Funcionalidades Principais (v1.0)

*   **Super Parser Heurístico:** Copie e cole mensagens despadronizadas enviadas por clientes (textos corridos, linhas sem rótulo, fichas fora de formatação). O sistema automaticamente extrai Nome, E-mail, Telefone, Cidade, Datas e soma automaticamente guias/motoristas aos hóspedes.
*   **Cálculo Automático de Diárias:** Reconhece entrada antecipada (Early Check-in) e saída tardia (Late Check-out) a partir dos horários digitados, e soma corretamente frações de +0,5 na diária.
*   **Renderizador Visual de Markdown:** O preview exibe os orçamentos exatamente como eles ficarão após enviados no WhatsApp (negrito, itálico, listas).
*   **Exportação Inteligente:**
    *   Cópia instantânea para área de transferência em markdown compatível com WhatsApp.
    *   **Impressão Nativa em PDF:** Um layout A4 elegante em folha branca (impresso localmente), desvinculado do tema web, perfeito para uso corporativo.
    *   **Banco de Clientes (CSV):** Histórico de todos os clientes salvos e opção para exportar planilhas `.csv` em formato UTF-8, pronto para Excel.
*   **100% Offline e Arquitetura Serverless:** O sistema roda totalmente a partir de um único arquivo `.html` utilizando Vanilla JavaScript, CSS3 e `LocalStorage` do navegador, não exigindo instalação ou custos mensais de servidores de banco de dados. Conta com rotinas de backup e restauração manual via `.json`.

## 🛠 Como utilizar

Por se tratar de um arquivo local e autônomo, o uso é extremamente simples:

1. Faça o download ou clone este repositório.
2. Abra o arquivo `orcamento.html` em qualquer navegador moderno (Chrome, Edge, Safari, Firefox).
3. (Opcional) Leve-o com você em um Pendrive ou envie para outros computadores.

> **Importante para transição entre PCs:** Como os dados ficam salvos localmente no navegador, sempre que precisar mudar de computador ou atualizar a versão do `.html`, vá em `Configurações > Exportar Backup (JSON)` na máquina antiga, abra o sistema na nova máquina e vá em `Configurações > Restaurar Backup (JSON)`.

## 🎨 Tecnologias Utilizadas

*   **HTML5 & CSS3:** Com variáveis customizáveis (Design System) permitindo temas Light/Dark dinâmicos sem Flash of Unstyled Content (FOUC).
*   **Vanilla JavaScript (ES6):** Toda a manipulação do DOM e a heurística de RegEx ocorrem no front-end em milissegundos, sem latência.
*   **Web APIs Nativas:** `LocalStorage`, `Clipboard API`, `Blob` e `FileReader` para uma experiência de desktop no navegador.

## 📌 Licença

Uso livre e gratuito. Sinta-se à vontade para modificar as configurações de quartos (`roomsPriceList`), regras de horários de late/early check-in e mensagens base diretamente no JSON da constante `DEFAULT_CONFIG` no final do script.
