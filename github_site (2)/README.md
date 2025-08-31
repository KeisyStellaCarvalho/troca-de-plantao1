# Site de Solicitação de Troca de Plantão

Este repositório contém um site estático simples para hospedar um formulário de solicitação de troca de plantão e uma página de perguntas frequentes (FAQ). O objetivo é permitir que os colaboradores enviem pedidos de troca sem necessidade de login e ao mesmo tempo disponibilizar informações úteis sobre o processo, em conformidade com a LGPD.

## Estrutura

Este repositório contém um site estático composto pelos seguintes arquivos:

* **index.html** – Página inicial. Contém um formulário HTML completo para solicitar trocas de plantão ou repasses de plantão. O formulário envia os dados por meio do serviço gratuito **FormSubmit** e apresenta um aviso sobre coleta de dados. Você deve editar este arquivo para informar seu endereço de e‑mail (no atributo `action`) e ajustar a URL de redirecionamento após o envio.
* **faq.html** – Lista de perguntas frequentes e respostas relacionadas à troca de plantão, utilizando elementos `<details>` para expandir/contrair cada item.
* **privacy.html** – Política de privacidade simplificada, explicando como os dados são coletados, utilizados e protegidos em conformidade com a LGPD.
* **thanks.html** – Página de agradecimento, exibida após o envio do formulário.
* **README.md** – Este arquivo com instruções de utilização.

## Como usar

1. **Clone ou crie o repositório no GitHub**
   - Crie um novo repositório no GitHub com um nome apropriado (por exemplo, `troca-plantao-site`).
   - Clone o repositório em sua máquina local ou simplesmente faça upload dos arquivos presentes nesta pasta.

2. **Configure o formulário interno**
   - Abra o arquivo `index.html` em um editor de texto.
   - Localize a tag `<form>` e substitua `SEU_EMAIL_AQUI` no atributo `action` pelo endereço de e‑mail que deve receber as solicitações. O FormSubmit enviará as respostas para este e‑mail.
   - Substitua também `SEU_USUARIO` e `NOME_REPOSITORIO` no valor do campo oculto `_next` pela URL do seu site no GitHub Pages. Esse campo define para onde o usuário será redirecionado após enviar a solicitação (por exemplo, `https://seu-usuario.github.io/troca-de-plantao-site/thanks.html`).
   - Opcionalmente, ajuste o campo oculto `_subject` para personalizar o assunto do e‑mail de notificação e adicione um campo `_cc` (veja a [documentação do FormSubmit](https://formsubmit.co/) para mais recursos, como envio de cópia para o gestor ou substituto).

3. **Commit e push**
   - Faça commit das alterações e envie para o GitHub com os comandos:

        git add .
        git commit -m "Configurar endereço de e-mail e redirecionamento"
        git push origin main

4. **Ativar o GitHub Pages**
   - No repositório, acesse **Settings → Pages**.
   - Em **Source**, selecione a branch (geralmente `main`) e a pasta `/ (root)` onde estão os arquivos. Salve as alterações.
   - O GitHub Pages gerará uma URL (por exemplo, `https://seu-usuario.github.io/nome-do-repositorio`) onde o site ficará disponível publicamente.

5. **Compartilhar o link**
   - Depois de publicar, compartilhe a URL do GitHub Pages com a equipe. O formulário interno não exige login; os colaboradores preenchem os campos necessários e enviam a solicitação, que será encaminhada por e‑mail para aprovação.

## LGPD

Lembre-se de adaptar a política de privacidade conforme as necessidades de sua organização, descrevendo claramente como os dados serão coletados, usados e protegidos. É importante que os colaboradores sejam informados sobre seus direitos e que seja solicitado consentimento explícito para o processamento de seus dados.