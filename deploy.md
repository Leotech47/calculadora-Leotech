# Calculadora LeoTech - Deploy na Vercel

Este guia explica como realizar o deploy da aplicação **Calculadora LeoTech** na Vercel, utilizando o repositório oficial hospedado no GitHub.

---

## 🔧 Pré-requisitos

* Conta no [GitHub](https://github.com/)
* Conta na [Vercel](https://vercel.com/)
* Node.js instalado localmente (opcional)

---

## 🚀 Passo a Passo

### 1. Acesse o Repositório

O código-fonte da aplicação está disponível no GitHub: [https://github.com/leotech47/calculadora-moderna](https://github.com/leotech47/calculadora-moderna)

### 2. Importe o Projeto para a Vercel

* Acesse [https://vercel.com](https://vercel.com) e faça login com sua conta do GitHub.
* Clique em **"New Project"**.
* Selecione o repositório **`calcular-moderna`**.
* A Vercel detectará automaticamente que o projeto é uma aplicação estática e configurará as opções necessárias.
* Clique em **"Deploy"** para iniciar o processo.([Medium][1], [docs.astro.build][2], [Vercel][3])

Após o deploy, a aplicação estará disponível em um subdomínio no formato `nomedousuario.vercel.app`.

### 3. (Opcional) Deploy via Vercel CLI

Se preferir utilizar a linha de comando, siga os passos abaixo:

* Instale a Vercel CLI:([Vercel][4])

```bash
  npm i -g vercel
```



* No diretório raiz do projeto, execute:

```bash
  vercel --prod
```



Isso vinculará seu diretório local ao projeto na Vercel e criará um deploy de produção. ([Vercel][5])

---

## 📌 Observações

* O deploy na Vercel é gratuito e ideal para aplicações estáticas.
* Alterações no código-fonte podem ser feitas diretamente no GitHub, e a Vercel realizará o deploy automaticamente.
* Para personalizar o comportamento do deploy, é possível utilizar o arquivo `vercel.json`.([Vercel][6])

---

## 📄 Licença

Este projeto está licenciado sob a licença MIT.

---

Para mais informações sobre como hospedar sites estáticos na Vercel, confira o vídeo abaixo:([YouTube][7])

[Como Hospedar seu site HTML, CSS, e JavaScript na Vercel](https://www.youtube.com/watch?v=JhIPcDpgNGw)

[1]: https://medium.com/%40lgoesmontes/como-fazer-o-deploy-do-meu-site-em-3-passos-com-o-vercel-f3619cab4d0b?utm_source=chatgpt.com "Como fazer o deploy do meu site em 3 passos com o Vercel"
[2]: https://docs.astro.build/pt-br/guides/deploy/vercel/?utm_source=chatgpt.com "Faça o deploy do seu site Astro na Vercel | Docs"
[3]: https://vercel.com/guides/deploying-react-with-vercel?utm_source=chatgpt.com "How to Deploy a React Site with Vercel"
[4]: https://vercel.com/guides/deploying-vuejs-to-vercel?utm_source=chatgpt.com "How to Deploy a Vue.js Site with Vercel"
[5]: https://vercel.com/docs/deployments?utm_source=chatgpt.com "Deploying to Vercel"
[6]: https://vercel.com/docs/cli/deploy?utm_source=chatgpt.com "vercel deploy"
[7]: https://www.youtube.com/watch?v=JhIPcDpgNGw&utm_source=chatgpt.com "Como Hospedar seu site HTML, CSS, e JavaScript na Vercel ..."

---

