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

O código-fonte da aplicação está disponível no GitHub: [https://github.com/leotech47/calculadora-moderna-Leotech](https://github.com/leotech47/calculadora-moderna-Leotech)

### 2. Importe o Projeto para a Vercel

* Acesse [https://vercel.com](https://vercel.com) e faça login com sua conta do GitHub.
* Clique em **"New Project"**.
* Selecione o repositório **`calculadora-moderna-Leotech`**.
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

# Guia — Registrar domínio no Registro.br e vincular à aplicação na Vercel (PASSO A PASSO)

Abaixo um guia objetivo, claro e conciso para **comprar um domínio no Registro.br**, **atribuir ao projeto na Vercel**, \*\* configurar o DNS no Registro.br\*\* e **testar** se o domínio já está funcionando.

---

## 1) Comprar domínio no Registro.br

1. Acesse **registro.br** → clique em **Entrar / Criar conta** e faça login.
2. Na barra de busca, digite o domínio desejado (ex.: `meusite.com.br`) e verifique disponibilidade.
3. Se disponível, clique em **Registrar**, preencha os dados solicitados (titular, contatos) e finalize a compra (checkout / pagamento).
4. Após confirmação, o domínio aparecerá no seu **Painel → Meus domínios**.

---

## 2) Adicionar o domínio no painel da Vercel

1. Entre na **Vercel** → abra o **projeto** da aplicação.
2. Vá em **Settings → Domains** (Configurações → Domínios).
3. Clique em **Add Domain / Adicionar domínio** e informe o domínio (ex.: `meusite.com.br`).
4. A Vercel mostrará instruções de verificação e os **registros DNS** ou **nameservers** que você deve configurar no Registro.br. **Copie** essas instruções — é o que a Vercel espera que você configure.

> Observação: a Vercel pode pedir que você use **nameservers da Vercel** (delegação) ou **registros DNS específicos** (CNAME / A / TXT). Use o método que preferir conforme necessidade (ver seção 3).

---

## 3) Configurar DNS no Registro.br

Você tem **duas opções** — escolha a que for melhor para você:

### Opção A — **Delegar nameservers** à Vercel (recomendado se não for usar e-mail no domínio)

1. No **Registro.br → Painel → clique no domínio**.
2. Localize **Servidores DNS** → clique em **Alterar servidores DNS**.
3. Substitua pelos nameservers fornecidos pela Vercel (ex.: `ns1.vercel-dns.com` e `ns2.vercel-dns.com`).
4. Salve. O Registro.br mostrará que a delegação está em processo.

**Vantagem:** Vercel administra DNS automaticamente (mais simples).
**Desvantagem:** pode dificultar configuração de e-mail ou outros serviços fora da Vercel.

---

### Opção B — **Manter DNS no Registro.br e adicionar registros manualmente** (recomendado se usar e-mail)

1. No **Registro.br → Painel → Editar Zona DNS** (ou “Editar Registros DNS”).
2. No painel da Vercel você verá os registros que devem ser criados — por exemplo:

   * **CNAME** para `www` apontando para o alvo indicado pela Vercel;
   * **A** ou **ALIAS/ANAME** para o domínio raiz (se a Vercel pedir);
   * **TXT** (para verificação) — se solicitado pela Vercel.
3. Crie exatamente os registros solicitados pela Vercel e salve.

**Vantagem:** mantém controle total (útil para e-mail).
**Desvantagem:** exige inserir registros manualmente.

---

## 4) Verificar e finalizar na Vercel

1. Volte ao **Settings → Domains** do projeto na Vercel.
2. A Vercel fará verificação automática — o status deve mudar para **Configuração válida / Verified** quando o DNS já estiver propagado.
3. Se aparecer erro, clique em **Re-check / Update** ou verifique os registros no Registro.br.

---

## 5) Como testar se o domínio está acessível (comandos e verificações)

* **Abrir no navegador**: acesse `https://seu-dominio.com.br`.
* **nslookup** (Windows/macOS/Linux):

  ```bash
  nslookup calculadoraleotech.com.br
  ```

  → Verifique se retorna IP ou referência para a Vercel (ou IP do provedor).
* **dig** (Linux/macOS):

  ```bash
  dig +short calculadoraleotech.com.br
  dig +short www.calculadoraleotech.com.br
  ```
* **curl** para verificar resposta HTTP:

  ```bash
  curl -I https://calculadoraleotech.com.br
  ```

  → Deve retornar `HTTP/1.1 200` ou redirecionamento válido.
* **Ferramentas online**: use *DNS Checker* (dnschecker.org) para ver propagação global.
* **Verificar status na Vercel**: em Domains, verificar **Configuração válida**.

**Limpeza de cache local**

* Windows: `ipconfig /flushdns`
* macOS: `sudo killall -HUP mDNSResponder`
* Navegador: abrir aba anônima ou limpar cache.

---

## 6) Problemas comuns e como resolver (rápido)

* **Status “Configuração inválida” na Vercel** → verifique se os registros no Registro.br correspondem exatamente aos que a Vercel pediu; remova registros antigos conflitantes.
* **CNAME no domínio raiz** → alguns registradores não aceitam CNAME no apex; prefira delegar nameservers ou usar as instruções da Vercel (A/ALIAS).
* **SSL/HTTPS não funciona** → aguarde a verificação DNS e a emissão do certificado pela Vercel; em seguida o HTTPS é provisionado automaticamente.
* **E-mail não funciona após delegar nameservers** → você perdeu os registros MX no Registro.br; se precisa de e-mail, prefira a Opção B (registros manuais) ou adicione os registros de e-mail no painel do provedor DNS que estiver utilizando.

---

## 7) Resumo rápido (fluxo mínimo)

1. Comprar domínio no Registro.br.
2. Adicionar domínio na Vercel (Settings → Domains).
3. No Registro.br: **ou** delegar nameservers para a Vercel **ou** criar os registros DNS indicados pela Vercel.
4. Verificar na Vercel o status **Configuração válida**.
5. Testar com `nslookup`, `dig`, `curl` e no navegador.

---


Perfeito 👌 Segue um **checklist curto e prático** para você usar no **Registro.br** e na **Vercel**.

---

# ✅ Checklist — Registro.br + Vercel

### 🔹 Etapa 1 — Registrar o domínio

* [ ] Acesse **[Registro.br](https://registro.br/)**
* [ ] Pesquise e registre o domínio desejado
* [ ] Confirme o pagamento e veja o domínio listado no painel

---

### 🔹 Etapa 2 — Adicionar o domínio na Vercel

* [ ] Entre no **painel da Vercel**
* [ ] Vá em **Settings → Domains** no projeto
* [ ] Clique em **Adicionar Domínio**
* [ ] Digite o domínio (`seudominio.com.br`)
* [ ] Copie as instruções de DNS (nameservers ou registros) fornecidas pela Vercel

---

### 🔹 Etapa 3 — Configurar DNS no Registro.br

1. No **painel do Registro.br**, clique sobre o domínio

2. Vá até **Servidores DNS**

   * [ ] Se optar por **delegar para a Vercel**:

     * Inserir:

       ```
       ns1.vercel-dns.com
       ns2.vercel-dns.com
       ```
   * [ ] Se optar por **configurar manualmente**:

     * Acesse **Editar Zona DNS**
     * Adicione os registros **CNAME/A/TXT** que a Vercel indicar

3. Clique em **Salvar Alterações**

4. Verifique se aparece a mensagem de **transição de DNS**

---

### 🔹 Etapa 4 — Aguardar propagação

* [ ] Esperar entre **30 min e 2h** (até 24h em alguns casos)
* [ ] Voltar na Vercel e checar se o domínio aparece como **Configuração válida**

---

### 🔹 Etapa 5 — Testar domínio

* [ ] No navegador: acessar `https://seudominio.com.br`
* [ ] No terminal (Windows):

  ```bash
  nslookup seudominio.com.br
  ```
* [ ] No Linux/macOS:

  ```bash
  dig +short seudominio.com.br
  ```
* [ ] Ferramenta online: [DNS Checker](https://dnschecker.org)

---

👉 Se todos os testes retornarem IPs ou apontarem para a Vercel e o navegador abrir sua aplicação, o domínio está funcionando corretamente! 🎉

---

