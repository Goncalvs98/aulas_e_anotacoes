### 🔹 **Estrutura Básica de um Documento HTML**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Página</title>
</head>
<body>
    <h1>Olá, mundo!</h1>
    <p>Bem-vindo à minha página.</p>
</body>
</html>
```

---

### 🔹 **Tags Essenciais**

|Tag|Descrição|
|---|---|
|`<h1>` a `<h6>`|Títulos (h1 é o maior, h6 o menor)|
|`<p>`|Parágrafo|
|`<a href="">`|Link|
|`<img src="" alt="">`|Imagem|
|`<ul>`, `<ol>`, `<li>`|Listas não ordenadas e ordenadas|
|`<div>`|Contêiner genérico|
|`<span>`|Contêiner inline|
|`<br>`|Quebra de linha|
|`<hr>`|Linha horizontal|

---

### 🔹 **Links e Imagens**

```html
<a href="https://www.google.com" target="_blank">Ir para o Google</a>

<img src="imagem.jpg" alt="Descrição da imagem" width="300">
```

---

### 🔹 **Tabelas**

```html
<table border="1">
    <tr>
        <th>Nome</th>
        <th>Idade</th>
    </tr>
    <tr>
        <td>Ana</td>
        <td>25</td>
    </tr>
</table>
```

---

### 🔹 **Formulários**

```html
<form action="processa.php" method="POST">
    <label for="nome">Nome:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <button type="submit">Enviar</button>
</form>
```

---

### 🔹 **Elementos Semânticos (SEO Friendly)**

|Tag|Uso|
|---|---|
|`<header>`|Cabeçalho da página|
|`<nav>`|Navegação|
|`<main>`|Conteúdo principal|
|`<section>`|Seção de conteúdo|
|`<article>`|Artigo ou post independente|
|`<aside>`|Barra lateral ou informações extras|
|`<footer>`|Rodapé da página|

Exemplo:

```html
<header>
    <h1>Meu Site</h1>
    <nav>
        <a href="#">Home</a>
        <a href="#">Sobre</a>
    </nav>
</header>
```

---

### 🔹 **Vídeos e Áudio**

```html
<video controls width="400">
    <source src="video.mp4" type="video/mp4">
    Seu navegador não suporta vídeos.
</video>

<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Seu navegador não suporta áudio.
</audio>
```

---

### 🔹 **Meta Tags Importantes**

```html
<meta name="description" content="Descrição breve da página">
<meta name="keywords" content="HTML, CSS, Web">
<meta name="author" content="Seu Nome">
<meta name="robots" content="index, follow">
```

---

### 🔹 **Favicons (Ícone do Site)**

```html
<link rel="icon" type="image/png" href="favicon.png">
```

---

### 🔹 **Boas Práticas**

✅ **Usar HTML semântico** para melhorar acessibilidade e SEO  
✅ **Incluir `alt` em imagens** para acessibilidade  
✅ **Usar `title` descritivo** para a página  
✅ **Fechar todas as tags corretamente**  
✅ **Manter um código organizado e indentado**
