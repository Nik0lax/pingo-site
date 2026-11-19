# Pingo — Landing page comercial (v2)

Landing page estática, criada para o GitHub Pages: **sem frameworks, sem Node, sem API e sem formulário**. Todos os estilos e interações estão dentro de `index.html`.

## O que mudou

- Nova identidade comercial em tons de azul/ciano, com hero, interface ilustrativa e mensagens focadas no produto.
- Animações de entrada ao rolar, glow sutil do cursor, barras de áudio, elementos flutuantes, status de navegação e barra de progresso de leitura.
- Painel interativo com exemplos de comandos (simulado, **não** envia pedidos ao Pingo).
- Demonstrações com os **três vídeos reais** fornecidos, com botão de pausa/reprodução e pausa automática fora da tela.
- Página responsiva para desktop, tablet e celular, com menu móvel acessível.
- Compatibilidade com `prefers-reduced-motion` para quem prefere animações reduzidas.
- Formulário e chamadas de inscrição removidos. A seção de disponibilidade comunica que **as licenças gratuitas do piloto estão esgotadas**.
- Informações de privacidade atualizadas para distinguir processamento de voz local de integrações de IA e outros serviços online.

## Estrutura dos arquivos

```text
pingo-site/
├── index.html
├── README.md
└── demos/
    ├── olhar.mp4
    ├── whatsapp.mp4
    ├── converter.mp4
    ├── olhar-poster.jpg
    ├── whatsapp-poster.jpg
    └── converter-poster.jpg
```

## Publicação no repositório existente

**Repositório:** https://github.com/Nik0lax/pingo-site

Opção simples: substitua o `index.html` da raiz pelo novo arquivo e mantenha ou substitua os três vídeos em `demos/` pelos fornecidos. Também pode subir este `README.md`.

Ou pelo terminal, dentro de um clone existente do repositório:

```bash
# Copie index.html, README.md e a pasta demos/ para a raiz do repositório.
git add index.html README.md demos/
git commit -m "feat: reformula landing page comercial do Pingo"
git push origin main
```

Se o GitHub Pages ainda não estiver configurado: **Settings → Pages → Deploy from a branch → main / (root)**.

Endereço esperado, se o GitHub Pages estiver habilitado: https://nik0lax.github.io/pingo-site/

## Personalização rápida

- Cores: seção `:root` do CSS, no início de `index.html`.
- Contato: busque por `pingo.ia.nik0lax@gmail.com`.
- Aviso do piloto: seção `<section ... id="disponibilidade">`.
- Textos e funcionalidades: seções `#recursos`, `#experimente`, `#demos`.
- Vídeos: substitua os arquivos em `demos/` preservando os nomes.
- Futuros lançamentos: se disponibilizar novas licenças, atualize a mensagem de disponibilidade manualmente. Não há lista de espera, formulário ou sistema de pagamento implementados.

## Notas técnicas

- Por ser HTML/CSS/JS puro, funciona no GitHub Pages sem processo de build.
- Os caminhos de vídeo são relativos (`demos/*.mp4`), adequados para URLs com `/pingo-site/`.
- Não são carregados pacotes JS externos e não há código de rastreamento.
- Reproduções de vídeo são silenciosas, em loop e apenas em áreas visíveis. O navegador pode restringir reprodução automática por decisão própria.
- A interface do hero é **ilustrativa**, e o painel de comandos é **uma simulação interativa**. As gravações nas seções de demonstração mostram as capturas reais fornecidas.

Os arquivos `*-poster.jpg` são imagens extraídas das gravações e aparecem caso o navegador bloqueie o autoplay.
