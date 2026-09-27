# Projeto Lista de Amigos — Sistema de Login e CRUD

Apresentação da atividade **Fichário — Agenda 08** da disciplina **Programação WEB II**

O material mostra como o cadastro de amigos (CRUD) foi evoluído com um sistema de login em PHP.

## Conteúdo do repositório

| Arquivo | Descrição |
|---|---|
| `lista_de_amigos_login_crud.pptx` | Apresentação com 10 slides sobre o projeto |
| `README.md` | Este arquivo |

## Roteiro da apresentação

1. **Capa** — Sistema de Login e CRUD
2. **Visão geral** — objetivo do projeto e tecnologias utilizadas
3. **Arquitetura de arquivos** — fluxo entre as páginas e arquivos de apoio (`include` / `require`)
4. **Banco de dados** — tabela `usuario` no banco `pwii`
5. **Tela de login** — formulário do `index.php`
6. **Autenticação** — validação no `loginAction.php` com MySQLi
7. **Sessões PHP** — `session_start()` e `$_SESSION`
8. **Bloqueio de acesso por URL** — `verificarAcesso.php`, `acessoNegado.php` e logout
9. **Cookies** — `setcookie()` e tempo de vida
10. **Competências desenvolvidas** — resumo do aprendizado

## AGENDA 08 DS II

- PHP
- MySQL com MySQLi
- HTML e W3.CSS
- Sessões e cookies

## Estrutura do projeto apresentado

```
index.php            → formulário de login
loginAction.php      → valida usuário e senha no banco
principal.php        → página principal do CRUD (protegida)
logoutAction.php     → encerra a sessão
conexaoBD.php        → conexão centralizada com o banco
cabecalho.php        → cabeçalho HTML compartilhado
rodape.php           → rodapé HTML compartilhado
verificarAcesso.php  → confere se há sessão ativa
acessoNegado.php     → tela exibida sem login
```

## Banco de dados

```sql
CREATE TABLE `pwii`.`usuario` (
  `idusuario` INT NOT NULL AUTO_INCREMENT,
  `nome` VARCHAR(45) NOT NULL,
  `senha` VARCHAR(45) NOT NULL,
  PRIMARY KEY (`idusuario`)
);

INSERT INTO `pwii`.`usuario` (`nome`, `senha`) VALUES ('gabi', 'gabi123');
```

## Como visualizar

Baixe o arquivo `lista_de_amigos_login_crud.pptx` e abra no PowerPoint, no LibreOffice Impress ou no Google Slides.
