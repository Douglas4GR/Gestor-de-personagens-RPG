# 🗂️ Gestor de Personagens – Genshin Impact  
Aplicação desenvolvida em **.NET 6 (MVC)** para ajudar jogadores RPG, mais especificamente de **Genshin Impact** a organizar seus personagens, equipamentos e atributos.  
Com muitos personagens no jogo, administrar recursos pode se tornar difícil — este projeto foi criado para facilitar esse gerenciamento.

---

## 🚀 Tecnologias Utilizadas
- **.NET 6**
- **ASP.NET MVC**
- **Entity Framework Core**
- **Razor Views**
- **Bootstrap / CSS Customizado**
- **jQuery + jQuery Validation**
- **Javascript (controllers simples em wwwroot)**

---

## 🎯 Funcionalidades
- Cadastro de personagens  
- Edição e exclusão  
- Visualização detalhada dos atributos  
- Separação de personagens e modelos (PersonagemModel)  
- Controle via repositório (abstração de acesso a dados)  
- Listagens com Razor Views  
- Tratamento de erros e layout compartilhado  

---

## 📂 Estrutura do Projeto

```
+---Controllers
|       HomeController.cs
|       Personagem.cs
|       PersonagemModelsController.cs
|
+---Data
|       BancoContext.cs
|
+---Models
|       ErrorViewModel.cs
|       PersonagemModel.cs
|
+---obj
|   \---Debug
|       \---net6.0
|
+---Properties
|       launchSettings.json
|
+---Repositorio
|       iPersonagemRepositorio.cs
|       PersonagemRepositorio.cs
|
+---Views
|   |   _ViewImports.cshtml
|   |   _ViewStart.cshtml
|   |
|   +---Home
|   |       Index.cshtml
|   |       Privacy.cshtml
|   |
|   +---Personagem
|   |       Apagar.cshtml
|   |       Criar.cshtml
|   |       Detalhes.cshtml
|   |       Editar.cshtml
|   |       Index.cshtml
|   |
|   +---PersonagemModels
|   |       Create.cshtml
|   |       Delete.cshtml
|   |       Details.cshtml
|   |       Edit.cshtml
|   |       Index.cshtml
|   |
|   \---Shared
|           Error.cshtml
|           _Layout.cshtml
|           _Layout.cshtml.css
|           _ValidationScriptsPartial.cshtml
|
\---wwwroot
    |   favicon.ico
    |
    +---css
    |   |   site.css
    |   \---Imagens
    |           aloalo.png
    |           characters.jpg
    |
    +---js
    |   |   site.js
    |   \---AngularController
    |           main.js
    |           PersonagemController.js
    |
    \---lib
        +---jquery
        +---jquery-validation
        |   |   LICENSE.md
        |   \---dist
        \---jquery-validation-unobtrusive
```

---

## 🏗️ Arquitetura

### **MVC (Model–View–Controller)**
- **Models** → Representam dados do personagem.
- **Views** → Telas .cshtml para CRUD completo.
- **Controllers** → Fluxo das telas e validações.

### **Repository Pattern**
Pasta `/Repositorio` contém:
- `iPersonagemRepositorio` – interface
- `PersonagemRepositorio` – implementação

Isso melhora a organização, facilita manutenção e testes.

---

## 🛢️ Banco de Dados
Utiliza **Entity Framework Core** e um `BancoContext.cs`.

As configurações de conexão ficam em:
```
appsettings.json
├─ ConnectionStrings
```
---

## ▶️ Como Executar o Projeto

1. Instale o SDK do **.NET 6**.

2. Clone o repositório:
```bash
git clone https://github.com/SEU-USUARIO/SEU-REPO.git
```

3. Entre na pasta:
```bash
cd GestorGenshinCharacters
```

4. Restaure dependências:
```bash
dotnet restore
```

5. Execute:
```bash
dotnet run
```

6. Acesse no navegador:
http://localhost:5000
ou
https://localhost:7000
