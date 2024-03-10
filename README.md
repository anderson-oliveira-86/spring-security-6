# Projeto de Estudo: Spring Security com JWT

Autor: Anderson de Oliveira \
Data: 2021-08-29

## Objetivo
Este projeto tem como objetivo estudar e entender a implementação do Spring Security com JSON Web Tokens (JWT). \
O foco é aprender como configurar a autenticação e autorização usando Spring Security e JWT.

## Sobre Spring Security e JWT

Spring Security é um framework de segurança poderoso e altamente personalizável que fornece autenticação e autorização para aplicações Java. Ele é amplamente usado para proteger aplicações Spring Boot.

JSON Web Token (JWT) é um padrão aberto (RFC 7519) que define uma maneira compacta e independente de transmitir informações entre partes como um objeto JSON. Essas informações podem ser verificadas e confiáveis porque são assinadas digitalmente.

Neste projeto, usamos Spring Security para autenticação e autorização e JWT para gerenciar sessões de usuários.

## Classes importantes

- `UserDetails`: Interface central que fornece informações principais do usuário.
- `UserDetailsService`: Interface que é implementada para buscar detalhes do usuário.
- `SecurityFilterChain`: Interface para uma cadeia de filtros de segurança, que são invocados em ordem.
- `JwtService`: Classe responsável por gerar e validar tokens JWT.
- `OncePerRequestFilter`: Filtro base para garantir uma única execução por solicitação.
- `AuthenticationProvider`: Interface que representa um provedor de autenticação.
- `AuthenticationManager`: Interface que representa um gerenciador de autenticação.
- `PasswordEncoder`: Interface para codificar senhas.
- `BCryptPasswordEncoder`: Implementação de `PasswordEncoder` que usa BCrypt.

## Como o projeto funciona

O projeto usa Spring Security para autenticar usuários. Quando um usuário se registra ou faz login, um token JWT é gerado e retornado para o usuário. Este token deve ser incluído no cabeçalho de autorização das solicitações subsequentes.

O token JWT é verificado em cada solicitação para garantir que o usuário está autenticado. A verificação é feita pelo `JwtAuthenticationFilter`, que é um `OncePerRequestFilter` que extrai o token do cabeçalho de autorização.

O `JwtService` é responsável por gerar e validar tokens JWT. Ele usa a biblioteca JJWT para isso.

## Como executar o projeto

Para executar o projeto, você precisa ter o Java e o Maven instalados. Depois de clonar o repositório, você pode executar o projeto usando o comando Maven:

```bash
mvn spring-boot:run
```
Depois de iniciar o servidor, você pode acessar a API em http://localhost:8080.