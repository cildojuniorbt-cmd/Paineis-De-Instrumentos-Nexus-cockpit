# Painéis de Instrumentos – Nexus Cockpit

Catálogo oficial de painéis do app **Nexus Cockpit** para Euro Truck Simulator 2 e American Truck Simulator.
Os painéis aparecem automaticamente na aba **Comunidade** do app.

## Como o catálogo funciona

| Onde                         | O que fica lá                                          |
|------------------------------|--------------------------------------------------------|
| `catalogo.json`              | A lista de painéis que o app mostra                     |
| `miniaturas/`                | A imagem de prévia de cada painel (JPG ou PNG)          |
| **Releases → `paineis`**     | Os arquivos `.simhubdash` (aceita arquivos grandes)     |

## Como adicionar ou atualizar um painel

1. **Exporte o painel no SimHub**: Dash Studio → botão direito no painel → *Export*.
   Renomeie o arquivo para um nome simples, sem espaços nem acentos (ex.: `scania_113h.simhubdash`).
2. **Envie o arquivo para a Release `paineis`**: aba *Releases* → release **paineis** → ícone de lápis (*Edit*) →
   arraste o arquivo em *Attach binaries* → *Update release*.
   (Para atualizar um painel, apague o arquivo antigo da release antes de enviar o novo com o mesmo nome.)
3. **Envie a miniatura** para a pasta `miniaturas/` (*Add file → Upload files*). Uma captura do painel serve.
4. **Edite o `catalogo.json`** (ícone de lápis) e adicione um bloco igual ao do Nexus, trocando os dados.
   Ao atualizar um painel, **aumente a `versao`** (ex.: `1.0` → `1.1`) para o app avisar quem já tem.

Exemplo de bloco:

```json
{
  "id": "scania_113h",
  "nome": "Scania 113H",
  "autor": "Seu nome",
  "descricao": "Painel clássico do Scania 113H.",
  "versao": "1.0",
  "atualizado": "2026-11-07",
  "jogos": "ETS2",
  "tamanhoMB": 5,
  "miniatura": "miniaturas/scania_113h.jpg",
  "arquivo": "scania_113h.simhubdash"
}
```

Atenção às vírgulas entre os blocos: todos menos o último terminam com `},`.

## Regras de uso

- Cada painel pertence ao seu autor.
- Os painéis podem ser usados livremente no app Nexus Cockpit.
- É proibido vender os painéis ou republicá-los sem autorização do autor.
- Só são aceitos painéis cujo autor autorizou a publicação.
