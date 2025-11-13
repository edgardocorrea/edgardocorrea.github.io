
# Meu Portfólio Pessoal

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-222222?style=for-the-badge&logo=github)](https://edgardocorrea.github.io)
[![Jekyll](https://img.shields.io/badge/Jekyll-CC0000?style=for-the-badge&logo=jekyll)](https://jekyllrb.com/)

> Este repositório contém o código-fonte do meu portfólio profissional, desenvolvido com Jekyll e o tema Minimal Mistakes. O site foi criado para apresentar meus projetos, habilidades técnicas e certificações na área de infraestrutura de TI e redes.

##  Preview do Site

![Preview do Portfólio](./assets/images/screenshot-do-site.png)

##  Tecnologias Utilizadas

Este projeto foi construído com as seguintes tecnologias:

-   **Jekyll:** Gerador de sites estáticos.
-   **Minimal Mistakes:** Tema Jekyll flexível e responsivo.
-   **GitHub Pages:** Hospedagem gratuita e integração com Git.
-   **Markdown:** Linguagem de marcação para criar o conteúdo das páginas.
-   **HTML5 / SASS:** Estrutura e estilização do tema.

##  Estrutura do Projeto

Uma visão geral da estrutura de pastas e arquivos principais do projeto:

```
/
├── _config.yml          # Arquivo de configuração principal do Jekyll.
├── _data/               # Arquivos de dados (ex: menu de navegação).
├── _includes/           # Componentes reutilizáveis (header, footer, etc.).
├── _layouts/            # Layouts para as páginas do site.
├── _portfolio/          # Coleção de projetos em formato Markdown.
├── _sass/               # Arquivos de estilo (SASS) do tema.
├── assets/              # Arquivos estáticos (imagens, CSS, JS).
├── index.md             # Página inicial do site.
├── portfolio.md         # Página que lista todos os projetos.
└── certificacoes.md     # Página para exibir os badges do Credly.
```

##  Como Executar Localmente (exemplo)

Para rodar este portfólio em sua máquina local, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/edgardocorrea/edgardocorrea.github.io.git
    cd edgardocorrea.github.io
    ```

2.  **Instale as dependências do Ruby e do Jekyll:**
    *(Caso ainda não tenha o Jekyll instalado, siga o [guia oficial](https://jekyllrb.com/docs/installation/))*
    ```bash
    bundle install
    ```

3.  **Execute o servidor local:**
    ```bash
    bundle exec jekyll serve
    ```

4.  Acesse o site no seu navegador: `http://localhost:4000`

##  Agradecimentos

Este projeto utiliza o fantástico tema [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) desenvolvido por [Michael Rose](https://github.com/mmistakes).

---







