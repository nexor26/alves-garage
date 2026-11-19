# Alves Garage — Site de ar-condicionado automotivo

Site institucional e comercial de página única da **Alves Garage** (ar-condicionado automotivo, Praia da Brisa, Rio de Janeiro). O foco é converter visitantes em contatos pelo WhatsApp: botões com mensagem pronta, sintomas clicáveis e formulário de orçamento que abre a conversa já preenchida.

## Tecnologias

- HTML5, CSS3 e JavaScript puro (sem framework e sem etapa de build)
- Fontes do Google Fonts: Barlow Condensed e Inter
- Ícones e ilustração em SVG inline
- JSON-LD (schema.org) e Open Graph para SEO local e compartilhamento

Não há backend, banco de dados, autenticação nem APIs próprias. O formulário monta uma mensagem e abre `https://wa.me/5521983195439`.

## Estrutura

```
.
├── index.html   # página completa (HTML + CSS + JS)
├── README.md
└── .gitignore
```

## Instalação

Nenhuma dependência para instalar: não há `package.json` porque o projeto é estático.

## Variáveis de ambiente

Não há segredos nem credenciais, então não existe `.env`. Os dados de contato ficam em constantes no início do `<script>` de `index.html`:

- `B` — link base do WhatsApp (`https://wa.me/5521983195439`)
- `D` — mensagem padrão dos botões
- `S` — lista de serviços (confirmar com a empresa antes de publicar)

Os links do Instagram e do Google Maps estão nos `href` do HTML.

## Executar localmente

Abra o `index.html` no navegador, ou sirva a pasta:

```bash
python3 -m http.server 8000
# ou
npx serve .
```

Depois acesse http://localhost:8000.

## Deploy

Por ser um site estático, qualquer hospedagem serve:

- **GitHub Pages:** Settings > Pages > Source: `main` / `(root)`.
- **Netlify:** arraste a pasta no painel, ou conecte o repositório (sem comando de build, diretório `.`).
- **Vercel:** importe o repositório como projeto estático (sem build).

## Fotos

O site foi entregue sem fotografias. Para usar uma foto no topo, defina `--hero-img` na seção `.hero`, por exemplo `style="--hero-img:url(imagens/hero.jpg)"`. Use apenas fotos com licença de uso comercial e não apresente imagens de banco como se fossem da oficina real.

## Dependências de plataforma

Este projeto foi criado em uma conversa com o Claude, não no Base44, e **não depende de nenhum serviço exclusivo de plataforma**. Só ficam fora do repositório o link de pré-visualização hospedado na criação e o favicon definido na publicação (agora embutido no `index.html`).

## Pendências antes de publicar

- Confirmar com a empresa a lista real de serviços.
- Adicionar fotografias reais.
- Definir a URL final do site e uma imagem para o Open Graph (`og:url`, `og:image`).
