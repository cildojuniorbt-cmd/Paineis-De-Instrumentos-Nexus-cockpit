# Painéis de Instrumentos – Nexus Cockpit

Catálogo oficial de painéis do app **Nexus Cockpit** para Euro Truck Simulator 2 e American Truck Simulator.
Os painéis aparecem automaticamente na aba **Painéis da comunidade** do app.

## Como o catálogo funciona

| Onde                          | O que fica lá                                         |
|-------------------------------|-------------------------------------------------------|
| `catalogo.json`               | A lista de painéis que o app mostra                    |
| `miniaturas/`                 | A imagem de prévia de cada painel (JPG ou PNG)         |
| **Releases** (tag `Painéis`)  | Os arquivos `.simhubdash` e o APK do app               |

## Como adicionar um painel

> Deixe a **tradução automática do navegador desligada** no GitHub: ela traduz até o código e pode estragar o `catalogo.json`.

1. **Exporte o painel no SimHub**: Dash Studio → botão direito no painel → *Export*.
   Use um nome simples, sem espaços nem acentos (ex.: `scania_113h.simhubdash`).
2. **Envie o arquivo para a release**: *Releases* → release **Painéis** → lápis (*Edit*) →
   arraste o arquivo nos anexos → espere terminar → *Update release*.
3. **Copie o link do arquivo**: na release, botão direito no nome do arquivo → *Copiar endereço do link*.
4. **Envie a miniatura** para a pasta `miniaturas/`:
   https://github.com/cildojuniorbt-cmd/Paineis-De-Instrumentos-Nexus-cockpit/upload/main/miniaturas
5. **Edite o `catalogo.json`** e adicione um bloco novo dentro de `"paineis": [ ... ]`:

```json
    {
      "id": "scania_113h",
      "nome": "Scania 113H",
      "autor": "Seu nome",
      "descricao": "Painel clássico do Scania 113H.",
      "versao": "1.0",
      "atualizado": "2026-11-07",
      "jogos": "ETS2",
      "miniatura": "miniaturas/NOME_EXATO_DA_IMAGEM.png",
      "arquivo": "LINK_COPIADO_NO_PASSO_3"
    }
```

Regras do `catalogo.json`:
- Entre um bloco e outro vai uma **vírgula** (`},` antes do `{` seguinte). O último bloco **não** tem vírgula depois do `}`.
- O nome da miniatura precisa ser **exatamente** igual ao do arquivo (maiúsculas e extensão contam).
- O `id` nunca deve mudar depois de publicado (é como o app reconhece o painel instalado).
- O `nome` pode mudar à vontade.

Depois de salvar, o app mostra as mudanças em até ~5 minutos (cache do GitHub).

## Como atualizar um painel

1. Na release, apague o arquivo antigo e envie o novo (pode ser com outro nome; aí copie o link novo).
2. No `catalogo.json`, atualize o `arquivo` (se o link mudou) e **aumente a `versao`** (ex.: `1.0` → `1.1`).
   Quem já tem o painel vê o botão **Atualizar** no app.

## Como publicar uma versão nova do app

1. Envie o `NexusCockpit.apk` para a release e copie o link.
2. No `catalogo.json`, logo depois de `"versaoCatalogo": 1,`, coloque (ou atualize) o bloco:

```json
  "app": {
    "versao": "1.2.0",
    "codigo": 3,
    "apk": "LINK_DO_APK",
    "notas": "O que mudou nesta versão"
  },
```

O app mostra o aviso **"Nova versão disponível"** quando o `codigo` daqui é maior que o da versão instalada.

## Regras de uso

- Cada painel pertence ao seu autor.
- Os painéis podem ser usados livremente no app Nexus Cockpit.
- É proibido vender os painéis ou republicá-los sem autorização do autor.
- Só são aceitos painéis cujo autor autorizou a publicação.
