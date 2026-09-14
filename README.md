# KARMED

Landing page do **KARMED — Emergências Médicas para Dentistas**: curso, app com IA clínica
e guia da maleta de emergência.

## Stack

Site estático de arquivo único. Não há build step, dependências nem `package.json`:
todo o HTML, CSS e JS vive inline em `index.html`.

## Estrutura

```
index.html            Página inteira (HTML + CSS + JS inline)
assets/
  hero.mp4            Vídeo do hero
  hero-poster.jpg     Poster do vídeo
  hero-end.jpg        Frame final do hero
  frames/             96 frames .webp da animação por scroll
  docentes/           Fotos dos docentes
  logo-karmed*.png    Logos (fundo claro e escuro)
  favicon.ico
source/               Material bruto de produção (não usado em runtime)
```

## Rodando localmente

Qualquer servidor estático na raiz do projeto serve:

```bash
python -m http.server 3000 --bind 127.0.0.1
```

Depois acesse http://127.0.0.1:3000

Abrir o `index.html` direto pelo `file://` também funciona, mas o vídeo do hero
e alguns assets podem se comportar de forma diferente por causa das restrições
de origem do navegador.

## Seções da página

`#top` (hero) · `#problema` · `#ecossistema` · `#curso` · `#app` · `#docentes`
· `#para-quem` · `#custo` · `#planos` · `#faq` · `#cta`
