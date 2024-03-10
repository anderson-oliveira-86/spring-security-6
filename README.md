# Projeto de Estudo: Spring Security com JWT

## Objetivo
Este projeto tem como objetivo estudar e entender a implementação do Spring Security com JSON Web Tokens (JWT). O foco é aprender como configurar a autenticação e autorização usando Spring Security e JWT.

## Passos
1. Configuração inicial do projeto com Spring Boot e dependências necessárias.
2. Implementação da classe de modelo do usuário.
3. Configuração do Spring Security e JWT.
4. Implementação do processo de autenticação e geração do token JWT.
5. Implementação do processo de validação do token JWT para autorização.
6. Testes para validar a autenticação e autorização.

## Classes Principais
- `User`: Representa o usuário no sistema. Contém informações como nome de usuário e senha.
- `JwtAuthenticationFilter`: Responsável pelo processo de autenticação e geração do token JWT.
- `JwtAuthorizationFilter`: Responsável pela validação do token JWT para autorização.
- `SecurityConfig`: Configurações do Spring Security.

Cada classe contém comentários de documentação detalhados explicando os pontos importantes implementados.

## Conclusão
Este projeto serve como um guia prático para entender como o Spring Security pode ser configurado para usar JWT para autenticação e autorização. Através do estudo e entendimento deste projeto, você será capaz de implementar esses conceitos em seus próprios projetos.
