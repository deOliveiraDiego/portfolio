# Portfólio: rascunho de copy (v2)

---

## Topo

**Diego de Oliveira**

Desenvolvo software há 8 anos. Hoje trabalho como product builder: converso com quem tem o problema, defino o escopo, construo e mantenho em produção.

[GitHub](https://github.com/deOliveiraDiego) · [LinkedIn](https://www.linkedin.com/in/deoliveiradiego) · [diego@deoliveiratech.com](mailto:diego@deoliveiratech.com)

---

## VERO

A VERO tinha a página de assinatura em WordPress. Era lenta, e o time precisava de terceiros para cadastrar condomínio ou saber quantos assinantes tinha. Fiz o escopo com eles, fechei o contrato e entreguei duas peças.

A primeira é a página de assinatura nova, em Astro estático, porque o que eles pediram primeiro foi velocidade. O formulário tem etapas, valida CPF e trava o envio duplicado. Essa trava entrou depois de um smoke test em produção mostrar que dois cliques podiam gerar dois cadastros.

A segunda é um admin em Next.js. Nele o time busca e edita assinantes, cadastra condomínios e acompanha os números por período. Na v1 o admin não apaga nada, só cria e edita, porque o time é pequeno e perder dado custaria mais do que ter um botão a menos. O banco só é acessado pelo servidor. Os testes rodam num Postgres local com dados fictícios, e o reset do banco se recusa a rodar fora da máquina local.

Também migrei os dados para contas da própria VERO. Hoje o time consulta, edita e exporta os contatos pelo painel, sem me chamar.

A página antiga levava cerca de 9 s para mostrar o conteúdo principal no celular. A nova leva 2,4 s (Lighthouse mobile, mediana de 3 medições, set/2026). [Rodar no PageSpeed agora](https://pagespeed.web.dev/analysis?url=https%3A%2F%2Fwww.vero.com.br%2Fassine-a-vero%2F&form_factor=mobile)

Astro, Next.js, TypeScript, Supabase, Postgres, Vitest, Playwright, Docker. Cerca de 150 testes nos dois projetos.

*Capturas de tela. O código é do cliente.*

---

## Conversando com o dado

Uma apresentação que fiz para mostrar a gente de negócio o que acontece quando um agente de IA consulta uma base de dados. A tela 4 tem um agente funcionando: você pergunta em português, ele gera o SQL, o banco executa, e ao lado aparecem a consulta, as linhas e o payload da requisição. Coloquei esse painel porque a pergunta que sempre aparece é "de onde veio esse número?".

A estrutura da base copia um export real de sellout. Os volumes são aleatórios.

*Demo · Repo*

---

## Calculadora do Cerrado

Uso para decidir onde colocar o aporte do mês numa carteira com alvo por ativo, sem vender nada. Informo quanto tenho em cada ativo e o valor do aporte, e ela divide o dinheiro entre os ativos que estão abaixo do alvo. Um dos ativos é em dólar e usa cotação ao vivo.

A conta fica numa função pura, separada da tela e da conversão de moeda. O arredondamento usa o método do maior resto, para a soma fechar no centavo. Depois de pronta, revisei a interface pelas heurísticas de Nielsen e corrigi o que apareceu. O caso mais sério: digitar "10.000" virava 1.

React, Vite, Vitest, Playwright. Deploy no GitHub Pages só com os testes passando.

*Demo · Repo*

---

## Outros

- **audio-transcript:** transcreve áudios longos com um modelo da NVIDIA rodando na própria máquina, sem custo por minuto. Python, FastAPI, Docker. *Repo*
- **Automações:** fluxos em n8n, integrações por API e agentes de atendimento para clientes.

---

## Como eu trabalho

Uso o Claude Code no dia a dia com um processo que montei para mim. Antes de codar, escrevo em cinco linhas o objetivo, o que entra, o que fica de fora, o caso que dá certo e o caso que dá errado. Depois vêm testes na lógica que importa, revisão da interface no navegador, revisão de segurança do diff e uma rodada de QA antes de entregar.

---

## Rodapé

[diego@deoliveiratech.com](mailto:diego@deoliveiratech.com) · [LinkedIn](https://www.linkedin.com/in/deoliveiradiego)
