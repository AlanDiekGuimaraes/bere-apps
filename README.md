# Bere Apps — páginas públicas

Política de privacidade e termos de uso de todos os jogos, em português, inglês e espanhol, publicados pelo GitHub Pages em https://alandiekguimaraes.github.io/bere-apps/.

O GitHub Pages compila o site com Jekyll a cada push na `main`; não há nada para instalar.

## Como está organizado

| Onde | O quê |
|---|---|
| `_includes/privacy/` e `_includes/terms/` | Os textos, um arquivo por idioma, iguais para todos os jogos |
| `_data/apps.yml` | Os dados de cada jogo (nome, o que guarda no aparelho, se tem recorde na conta Google ou doação, data da última mudança) |
| `_data/i18n.yml` | Títulos, nomes dos idiomas, formato de data e endereços das páginas |
| `<jogo>/...` | Seis arquivos curtos que só dizem qual jogo, qual texto e qual idioma |
| `novo-jogo/` | Modelo desses seis arquivos (não é publicado) |

Mudar um texto para todos os jogos: editar o arquivo em `_includes/` e atualizar a data `updated` dos jogos afetados em `_data/apps.yml`.

## Endereços de cada jogo

| | Privacidade | Termos |
|---|---|---|
| Português | `/<jogo>/privacidade/` | `/<jogo>/termos/` |
| English | `/<jogo>/en/privacy/` | `/<jogo>/en/terms/` |
| Español | `/<jogo>/es/privacidad/` | `/<jogo>/es/terminos/` |

## Adicionar um jogo novo

1. Em `_data/apps.yml`, copiar o bloco do `pocket-brick`, trocar o identificador (ex.: `grid-puzzle`) e preencher os campos.
2. Copiar a pasta `novo-jogo/` com o mesmo identificador e, nos seis `index.html`, trocar `ID-DO-JOGO` por ele.
3. Fazer push. A página inicial já lista o jogo novo.
4. Colocar o link da privacidade na Play Console e na tela Privacidade e termos do app.

Se o jogo tiver algo que os textos ainda não cobrem (uma permissão, um serviço novo), acrescentar um campo em `_data/apps.yml` e um bloco `{% if app.campo %}` nos seis textos.
