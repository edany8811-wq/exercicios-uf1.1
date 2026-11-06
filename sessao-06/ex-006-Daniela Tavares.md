# Exercício Prático: A Oficina de Olaria 🏺

Hoje demos voz aos visitantes do nosso portefólio, criando um formulário de contacto completo com controlos de texto, seletores, botões de opção e caixas de texto. Agora é a vossa vez: vão permitir que os visitantes do site da vossa cidade enviem recomendações de locais e construir do zero uma página de inscrição para uma oficina tradicional de olaria e cerâmica.

O vosso objetivo é dominar a criação de formulários semânticos e acessíveis, compreendendo a função de `<form>`, `<label>`, `<input>`, `<select>`, `<textarea>`, `<fieldset>`, `<legend>` e botões de ação.

Os ficheiros de que precisam estão na pasta [`ex-006/`](./ex-006/): `oficina-olaria.txt`.

### Missão 1: A Minha Cidade, Versão 6

1. Criem a pasta `sessao-06` dentro da vossa pasta `exercicios-uf1.1` e copiem para lá todo o conteúdo da pasta `sessao-05` (incluindo a pasta `imagens`).
2. Abram o ficheiro `cidade.html` e adicionem uma nova secção no `<main>` com o identificador `id="sugestoes"` e o título "Partilhe uma sugestão sobre a cidade":
   - Um parágrafo a convidar os visitantes a sugerirem novos pontos de interesse.
   - Um elemento `<form action="#" method="post">` organizado em dois grupos semânticos (`<fieldset>` com `<legend>`):
     - Grupo 1 ("A sua identificação"): campo de texto para o nome do visitante e campo de e-mail para contacto, ambos com as respetivas etiquetas `<label for="...">`.
     - Grupo 2 ("Detalhes da recomendação"):
       - Uma lista suspensa (`<select>`) com pelo menos 4 categorias (Monumento, Miradouro/Natureza, Restaurante/Gastronomia, Museu).
       - Um par de botões de rádio (`type="radio"`) com o mesmo atributo `name` para indicar se o utilizador é morador local ou turista.
       - Uma área de texto (`<textarea>`) com `rows` e `cols` para descrever o local sugerido.
       - Uma caixa de verificação (`type="checkbox"`) para autorizar a publicação da sugestão.
     - Dois botões de ação: `<button type="submit">` para enviar e `<button type="reset">` para limpar.
   - Adicionem o link para `#sugestoes` no menu de navegação (`<nav>`) do `<header>`.
3. Validem no [validador do W3C](https://validator.w3.org/#validate_by_input).
4. Façam o ciclo de trabalho no Git:
   - `git add .`
   - `git commit -m "Cidade com formulario de sugestoes"`
   - `git push`

### Missão 2: A Página da Oficina de Olaria de Barcelos

Vão estruturar uma página completa sobre o artesanato tradicional do barro e criar a respetiva ficha de pré-inscrição em workshops.

1. Copiem para a vossa pasta `sessao-06` o ficheiro [`oficina-olaria.txt`](./ex-006/oficina-olaria.txt).
2. Criem o ficheiro `oficina-olaria.html` com a estrutura base completa (`<!doctype html>`, `<html lang="pt-PT">`, `head`, `body`). O título do separador deve ser "Oficina de Olaria Tradicional de Barcelos".
3. Organizem o conteúdo através de elementos semânticos:
   - `<header>` com o título principal (`<h1>`), o texto de enquadramento histórico e um menu de navegação (`<nav>`) com links de âncora para as quatro secções (`#workshops`, `#horarios`, `#inscricao`, `#contactos`).
   - `<main>` dividido em quatro secções:
     - Secção "Workshops disponíveis" com três artigos (`<article>`), cada um descrevendo uma formação com `<h3>`, `<p>` e uma lista com marcas (`<ul>`) com duração e materiais.
     - Secção "Horários e modalidades" com uma tabela semântica (`<table>`) contendo `<caption>`, `<thead>`, `<tbody>`, e células `<th>` com atributo `scope`.
     - Secção "Ficha de pré-inscrição" com o formulário completo (`<form action="#" method="post">`):
       - `<fieldset>` para dados pessoais com campos para nome completo, correio eletrónico e telemóvel (`type="tel"`).
       - `<fieldset>` para opções de formação com `<select>` para escolher o workshop, botões de rádio para o regime de frequência (Pós-laboral ou Fim de semana), caixas de seleção (`type="checkbox"`) para os dias disponíveis (Terça, Quinta, Sábado), área de texto (`<textarea>`) para motivação ou experiência e uma caixa de autorização de contacto.
       - Botões de envio (`type="submit"`) e limpeza (`type="reset"`).
     - Secção "Contactos e localização" com morada, link `mailto:` e link externo seguro para o portal oficial com `target="_blank"` e `rel="noreferrer noopener"`.
   - `<footer>` com os direitos de autor (`&copy; 2026 Associação dos Artesãos e Oleiros de Barcelos`).
4. Validem no validador do W3C.
5. Façam o ciclo de trabalho no Git:
   - `git add .`
   - `git commit -m "Pagina da oficina de olaria com formulario de inscricao"`
   - `git push`

**Critérios de sucesso:**

- [ ] A pasta `sessao-06` tem `cidade.html` atualizado e `oficina-olaria.html` criado.
- [ ] Todos os campos de formulário têm uma `<label>` associada através do atributo `for` coincidente com o `id`.
- [ ] Todos os campos editáveis possuem o atributo `name` devidamente atribuído.
- [ ] Os botões de rádio partilham o mesmo `name`, permitindo selecionar apenas uma opção de cada vez.
- [ ] O menu de navegação de âncoras salta diretamente para as secções pretendidas.
- [ ] A tabela inclui legenda `<caption>` e cabeçalhos com atributo `scope`.
- [ ] O validador do W3C não devolve erros nem avisos de aninhamento inválido.
- [ ] O repositório no GitHub reflete todos os novos ficheiros e mensagens de commit.

A vossa pasta `exercicios-uf1.1` deve ficar assim:

```
exercicios-uf1.1/
├── sessao-01/
├── sessao-02/
├── sessao-03/
├── sessao-04/
├── sessao-05/
└── sessao-06/
    ├── imagens/
    │   ├── cidade.svg
    │   └── ovos-moles.svg
    ├── cidade.html
    ├── aldeias-historicas.txt
    ├── aldeias-historicas.html
    ├── oficina-olaria.txt
    └── oficina-olaria.html
```

### Missão 3: O Relatório

Respondam às seguintes questões por palavras vossas:

1. A diferença entre `name` e `id`:
   Qual é o papel do atributo `id` e do atributo `name` num campo de formulário? O que acontece aos dados introduzidos pelo utilizador quando um campo não tem o atributo `name`?
   Resposta: O id é a identidade do campo dentro da página: tem de ser único e serve para ligar coisas dentro do nosso próprio HTML — por exemplo, a <label for="nome"> liga-se ao campo através do id="nome", e as âncoras do menu também saltam para um id. O name tem outra função: é o nome com que os dados viajam quando o formulário é enviado — o servidor recebe pares de name=valor (por exemplo, regime=pos-laboral). Quando um campo não tem o atributo name, o que o utilizador escreveu não é enviado: o navegador ignora esse campo no momento do envio, como se nem existisse. Resumindo: o id é para a página, o name é para os dados.

2. Rótulos e acessibilidade:
   Porque é que colocar apenas um `placeholder` não substitui uma etiqueta `<label>`? Que comportamento útil acontece no navegador quando um utilizador clica em cima do texto de uma `<label>` corretamente configurada?
   Resposta: [O placeholder é apenas uma dica cinzenta escrita dentro do campo, que desaparece assim que começamos a escrever — a meio do preenchimento, a pessoa já não vê o que lhe foi pedido. Além disso, os leitores de ecrã usados por pessoas cegas nem sempre anunciam o placeholder e o texto cinzento tem pouco contraste, o que dificulta a leitura a quem tem baixa visão. A <label> é uma etiqueta permanente, sempre visível e corretamente associada ao campo. E há um comportamento muito útil: quando a label está bem configurada (com o for igual ao id do campo), clicar no texto da etiqueta faz o cursor saltar diretamente para dentro do campo — e numa checkbox ou num rádio, clicar no texto até marca a opção, o que ajuda muito em ecrãs pequenos.]

3. Rádios vs Checkboxes:
   Em que circunstâncias devemos utilizar botões de rádio (`type="radio"`) e em que casos devemos optar por caixas de verificação (`type="checkbox"`)? Qual é a regra técnica para que vários botões de rádio pertençam ao mesmo grupo de escolha exclusiva?
   Resposta: [O placeholder é apenas uma dica cinzenta escrita dentro do campo, que desaparece assim que começamos a escrever — a meio do preenchimento, a pessoa já não vê o que lhe foi pedido. Além disso, os leitores de ecrã usados por pessoas cegas nem sempre anunciam o placeholder e o texto cinzento tem pouco contraste, o que dificulta a leitura a quem tem baixa visão. A <label> é uma etiqueta permanente, sempre visível e corretamente associada ao campo. E há um comportamento muito útil: quando a label está bem configurada (com o for igual ao id do campo), clicar no texto da etiqueta faz o cursor saltar diretamente para dentro do campo — e numa checkbox ou num rádio, clicar no texto até marca a opção, o que ajuda muito em ecrãs pequenos.]

---

### 🚀 Desafio Bónus (Para os mais rápidos)

1. No formulário da oficina de olaria, apliquem o atributo `autofocus` no campo de nome para que a página abra com o cursor logo pronto para escrever.
2. Definam uma opção pré-selecionada no menu suspenso ou num dos botões de rádio utilizando os atributos booleanos `selected` ou `checked`.
3. Experimentem aplicar o atributo `disabled` num botão ou num campo de texto e observem como o navegador impede a edição e altera a aparência do controlo.

