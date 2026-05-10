# 🏗️ Stylo Arte — Serralheria & Vidraçaria

> **Site institucional completo** desenvolvido do zero para empresa com 28 anos de mercado em Itaquera, São Paulo. Do design cinematográfico à publicação no ar com domínio próprio, SEO avançado e Google Analytics configurado.

<br>

[![Site no Ar](https://img.shields.io/badge/🌐_Site_ao_Vivo-styloarteserralheria.com.br-1a3a6b?style=for-the-badge)](https://www.styloarteserralheria.com.br)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

---

## 🎬 O Projeto

O cliente tinha um site **desatualizado, com endereço errado, botão de WhatsApp levando para outra pessoa, e desenvolvedor que não respondia há meses.** A missão era clara: entregar algo que impressionasse — mantendo o mesmo domínio que o cliente já tinha.

Este repositório documenta o ciclo completo de desenvolvimento freelance: do primeiro contato com o cliente, negociação, desenvolvimento, ajustes, deploy e configuração de SEO/Analytics.

---

## ✨ Funcionalidades

| Feature | Descrição |
|---|---|
| 🎭 **Hero Cinematográfico** | Imagem de impacto gerada por IA + efeito typewriter + partículas flutuantes + parallax no scroll |
| 📸 **Galeria com Slideshow** | Cards por categoria de serviço com troca automática de fotos a cada 3s |
| 🎬 **Cards de Vídeo** | Suporte a vídeos `.webm` nos cards de galeria com badge "▶ Vídeo" |
| 📢 **Banner Animado** | Faixa superior com frases de chamada em loop infinito — pausa no hover |
| 📱 **100% Responsivo** | Mobile-first, menu hambúrguer com overlay, breakpoints em 768px e 1024px |
| ⚡ **Performance** | Imagens em WebP, lazy loading, `preload="none"` em vídeos, zero dependências externas |
| 🔢 **Contadores Animados** | Números animados de 0 ao valor final ativados por Intersection Observer |
| 💬 **FAQ Acordeões** | 6 perguntas frequentes com animação suave de abertura/fechamento |
| ⭐ **Depoimentos Esteira** | Carrossel infinito automático — pausa ao hover |
| 📬 **Formulário → WhatsApp** | Campos formatados e enviados diretamente para o WhatsApp do cliente |
| 🏢 **Modal Facebook** | Abre a página do Facebook do cliente em modal premium sem sair do site |
| 📷 **Modal Instagram** | Card elegante com link para o perfil do Instagram |
| 🔒 **Modais Legais** | Política de Privacidade, Termos de Uso e Cookies em modais — sem páginas separadas |
| 💚 **WhatsApp Flutuante** | Botão que expande com texto "Chama no Whats" ao hover |
| 🗺️ **Localização** | Card de localização com botão "Abrir no Google Maps" |
| 🔄 **Reveal no Scroll** | Elementos entram com fade-up, fade-left e fade-right ao aparecer na tela |

---

## 🛠️ Stack Técnica

```
Frontend
├── HTML5 semântico
├── CSS3 puro (variáveis, grid, flexbox, animações, keyframes)
└── JavaScript Vanilla (sem frameworks, sem dependências)

Performance
├── Imagens WebP (60-80% menor que JPEG)
├── Intersection Observer API (lazy animations)
├── Canvas API (partículas animadas)
└── Vídeos com preload="none"

Deploy & Infraestrutura
├── Vercel (hosting + SSL automático)
├── Registro.br (domínio .com.br)
└── DNS via Nameservers do Vercel (ns1/ns2.vercel-dns.com)

SEO & Analytics
├── Schema.org LocalBusiness (JSON-LD)
├── Open Graph + Twitter Card
├── Sitemap.xml com imagens indexadas
├── Robots.txt
├── Google Search Console verificado
├── Google Analytics 4 (GA4)
└── Google Business Profile atualizado
```

---

## 📁 Estrutura de Pastas

```
styloarteserralheria/
│
├── index.html              # Site completo (HTML + CSS + JS inline)
├── sitemap.xml             # Sitemap com imagens para indexação
├── robots.txt              # Instruções para crawlers
├── favicon.webp            # Ícone da aba do navegador
├── logo-styloarte.webp     # Logo da empresa
├── hero-principal.webp     # Imagem principal do hero
│
├── videos/
│   ├── divisorias-escritorio.webm
│   ├── persiana-automatizada.webm
│   └── persiana-automatizada-2.webm
│
└── imagens/
    ├── empresa/
    │   └── fachada.webp
    ├── fechamento-pia-escada/   → foto-1.webp … foto-38.webp
    ├── portas-aluminio/         → foto-1.webp … foto-21.webp
    ├── janelas-aluminio/        → foto-1.webp … foto-17.webp
    ├── portoes-aluminio/        → foto-1.webp … foto-8.webp
    ├── box-vidro/               → foto-1.webp … foto-21.webp
    ├── grades-corrimoes/        → foto-1.webp … foto-31.webp
    ├── guarda-corpo/            → foto-1.webp … foto-10.webp
    ├── expositores/             → foto-1.webp … foto-6.webp
    ├── portas-camarao/          → foto-1.webp … foto-11.webp
    └── telas-mosquiteiros/      → foto-1.webp … foto-17.webp
```

---

## 🚀 Como Adicionar Novas Fotos

1. Coloque as fotos na pasta correspondente em `imagens/nome-do-servico/`
2. Renomeie seguindo o padrão: `foto-1.webp`, `foto-2.webp`, ...
3. No `index.html`, encontre o array `const galerias` e adicione o nome do arquivo na lista `fotos`

```javascript
// Exemplo — adicionar foto-4 na galeria de box de vidro
{ titulo: 'Box de Vidro', pasta: 'box-vidro', fotos: [
  'foto-1.webp','foto-2.webp','foto-3.webp','foto-4.webp' // ← aqui
]}
```

---

## 🆕 Como Adicionar Novo Card de Serviço

```javascript
// Com fotos
{ titulo: 'Nome do Serviço', pasta: 'nome-da-pasta', fotos: ['foto-1.webp','foto-2.webp'] },

// Com vídeo
{ titulo: 'Nome do Serviço', pasta: 'pasta', video: 'videos/nome.webm', fotos: [] },
```

---

## 📊 Resultados Entregues

- ✅ Site do zero ao ar em domínio próprio
- ✅ Mesmo domínio mantido (cliente não queria trocar)
- ✅ Endereço correto e WhatsApp apontando para o número certo
- ✅ Google Search Console verificado e sitemap indexado
- ✅ Google Analytics 4 ativo
- ✅ Google Maps atualizado com nova logo, fotos e horários
- ✅ Performance superior ao site anterior em WordPress
- ✅ Zero dependências externas — sem jQuery, sem Bootstrap, sem nada

---

## 👨‍💻 Desenvolvedor

**João Roberto** — Desenvolvedor Web & Automações com IA

[![Instagram](https://img.shields.io/badge/@jrdev.ia-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/jrdev.ia)
[![WhatsApp](https://img.shields.io/badge/Contato-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/5511948135491)

---

*Projeto desenvolvido como freelance — do briefing ao deploy. Nenhuma API exposta. Nenhuma chave sensível no repositório.*
