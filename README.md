# FiveM-script-template

Um template de script moderno e otimizado para a criação de recursos no **FiveM**, estruturado de forma ideal para o ecossistema **Qbox Core** e **ox_lib**. Criado com as melhores práticas de gerenciamento de configurações, localização e versionamento de metadados.

## ✨ Características
- Pré-configurado para o ecossistema **qbx_core** e **ox_lib**.
- Força a tag Lua 5.4 (`lua54 'yes'`) no manifesto para performance otimizada, melhor *garbage collection* e adoção do padrão moderno da linguagem.
- Estrutura de diretórios sólida: separação declarada de scripts nas pastas `client/` e `server/`.
- Configurações isoladas na pasta `config/` nativamente protegidas com o recurso `escrow_ignore`. Ideal para quem criptografa seus códigos via CFX Keymaster, permitindo customizações seguras pelos donos de servidores usando `lib.load()`.
- Incorpora manipulação fluída do sistema de tradução (locales).

## 📂 Estrutura de Pastas

```text
├── client/           # Módulos e scripts do lado do cliente (client-side)
├── config/           # Arquivos de configurações (server.lua, client.lua e shared.lua)
├── locales/          # Dicionários JSON para traduções e mensagens com suporte ox_lib
├── server/           # Módulos e scripts do lado do servidor (server-side)
└── fxmanifest.lua    # Definição e empacotamento do recurso
```

## 🚀 Como Utilizar

1. Faça o download/clonagem da pasta no seu diretório `resources/`.
2. Renomeie a pasta de acordo com a necessidade (ex.: `meu-script-legal`).
3. Adicione o nome do recurso ao seu `server.cfg`:
   ```cfg
   ensure meu-script-legal
   ```

## 🛠 Bibliotecas e Dependências

Para que o script carregue da maneira esperada (vide referências no `fxmanifest.lua`), garanta que no seu servidor as seguintes dependências já estejam sendo iniciadas antes desse script:
- [ox_lib](https://github.com/overextended/ox_lib)
- [qbx_core](https://github.com/Qbox-project/qbx_core)

## ✍️ Autor
Gabarito Estrutural por **Dougg Junnior <douggjunn>**