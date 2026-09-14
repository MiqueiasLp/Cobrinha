# 🐍 GitHub Contribution Snake Animation Workflow

Este repositório contém uma automação usando **GitHub Actions** que gera uma animação em formato SVG da cobrinha (estilo *Snake Game*) comendo os quadradinhos de contribuição do seu perfil do GitHub.

---

## 🚀 Como Funciona?

O workflow é executado de forma automática e faz os seguintes passos:

1. **Gera a Animação:** Lê o seu gráfico de contribuições e cria um arquivo `.svg` temático no modo escuro (*github-dark*).
2. **Atualiza Automaticamente:** 
   - Executa a cada **12 horas**.
   - Executa sempre que houver um `push` na branch `main`.
   - Permite execução manual a qualquer momento via aba **Actions**.
3. **Publicação em Branch Separada:** O SVG gerado é enviado automaticamente para uma branch isolada chamada `output`.

---

## ⚙️ Configuração Inicial

Para que o workflow funcione corretamente no seu repositório:

1. Salve o arquivo de configuração em:  
   `.github/workflows/snake.yml`
2. **Permissões do GitHub Actions:**
   - Vá nas configurações do repositório: **Settings** > **Actions** > **General**.
   - Na seção **Workflow permissions**, selecione **Read and write permissions**.
   - Clique em **Save**.

---

## 🖼️ Como Exibir a Animação no seu Readme de Perfil

Após a primeira execução do workflow, a animação estará salva na branch `output`. 

Para exibir a cobrinha no seu `README.md` principal do perfil, adicione o seguinte trecho onde desejar:

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="[https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/output/github-contribution-grid-snake-dark.svg](https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/output/github-contribution-grid-snake-dark.svg)">
  <source media="(prefers-color-scheme: light)" srcset="[https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/output/github-contribution-grid-snake-dark.svg](https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/output/github-contribution-grid-snake-dark.svg)">
  <img alt="github snake animation" src="[https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/output/github-contribution-grid-snake-dark.svg](https://raw.githubusercontent.com/SEU_USUARIO/SEU_REPOSITORIO/output/github-contribution-grid-snake-dark.svg)">
</picture>
