<div align="center">

# Eficaz Contabilidade

**Site oficial da Eficaz Contabilidade, escritório de contabilidade rural e empresarial em São Borja (RS).**

[![Ver no ar](https://img.shields.io/badge/ver_no_ar-eficazcontabilidadesb.com.br-1D7A4F?style=for-the-badge&labelColor=18181B)](https://www.eficazcontabilidadesb.com.br)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)

</div>

<p align="center">
  <img src="docs/preview-desktop.webp" width="72%" alt="Site da Eficaz Contabilidade no computador">
  <img src="docs/preview-mobile.webp" width="22%" alt="Site da Eficaz Contabilidade no celular">
</p>

## Sobre

Site institucional e de captação de clientes da Eficaz Contabilidade. O foco é o produtor rural que precisa organizar a contabilidade para a Reforma Tributária (IBS e CBS a partir de 2027), sem deixar de lado empresas do Lucro Real, Lucro Presumido, Simples Nacional e MEIs.

Todo o contato acontece pelo WhatsApp: cada botão abre a conversa com uma mensagem pronta, e o formulário de orçamento monta o texto com o que a pessoa preencheu.

## Destaques

- **Livro-caixa rural animado no topo.** Um cartão simula notas de uma safra sendo lançadas uma a uma: cada nota desce para o fim da lista (animação FLIP), o total de despesas que geram crédito sobe com contagem animada e um aviso confirma o lançamento. Mostra na prática o argumento da Reforma Tributária.
- **Linha do tempo da Reforma Tributária** (2026, 2027, 2029 a 2032 e 2033) numa seção escura, com a lista do que pode virar crédito para o produtor.
- **Serviços em bento, por prioridade.** Rural, Lucro Real e Presumido, Simples Nacional e MEI, cada um com um mini painel ilustrativo: gráfico de despesas da safra, comparação de regimes, fechamento do mês e medidor do limite anual do MEI.
- **Animações que só rodam quando aparecem na tela.** Os ciclos de enche, segura e esvazia param quando o bloco sai da tela ou a aba fica em segundo plano, para não gastar bateria.
- **Formulário de orçamento que vira mensagem de WhatsApp.** Nome, situação (produtor rural, Lucro Real ou Presumido, Simples, MEI, abrir empresa, trocar de contador, Imposto de Renda) e cidade. Valida o nome, mostra estado de envio e uma tela de confirmação. Nenhum dado vai para servidor.
- **Botões magnéticos** com física de mola no computador, e botão flutuante de WhatsApp que aparece depois do topo e some sobre o formulário.
- **Mapa do Google** com esqueleto animado até o mapa carregar.
- **Medição de cliques.** Cada botão de WhatsApp registra um evento com o lugar onde foi clicado. O Google Analytics só mede no domínio oficial; testes locais e prévias ficam fora dos relatórios.
- **Aviso de cookies e política de privacidade** (LGPD) em página própria.

## Seções da página

1. **Topo:** chamada sobre o crédito de IBS e CBS, botões para contabilidade rural e serviços, e o livro-caixa animado.
2. **Faixa de obrigações:** letreiro contínuo com LCDPR, ITR, Funrural, SPED, eSocial, DAS e outras entregas.
3. **Reforma 2027:** o que muda para o produtor rural até 2033, em linha do tempo.
4. **Serviços:** contabilidade rural, Lucro Real e Presumido, Simples Nacional, MEI e uma lista de serviços extras (abertura de empresa, troca de contador, Imposto de Renda, folha e planejamento tributário).
5. **Como funciona:** três passos, do primeiro contato no WhatsApp até a rotina mensal.
6. **Por que a Eficaz:** motivos para escolher o escritório e chamada para avaliar no Google.
7. **Dúvidas:** perguntas frequentes em sanfona (`<details>`).
8. **Contato:** dados do escritório, mapa e formulário de orçamento.

## Tecnologias

| Camada | Ferramentas |
| --- | --- |
| Interface | HTML, CSS e JavaScript puros, sem framework e sem etapa de build |
| Animação | CSS (keyframes e transições), IntersectionObserver e Web Animations API |
| Tipografia e ícones | Geist e Geist Mono (Google Fonts), Phosphor Icons |
| Medição | Google Analytics 4 com eventos de clique |
| Hospedagem | Vercel, com domínio próprio |

## SEO, desempenho e acessibilidade

- Domínio próprio `.com.br`, com URL canônica e um redirecionamento permanente do endereço antigo da Vercel para o domínio oficial (`vercel.json`).
- `title` e `meta description` focados em contabilidade rural e empresarial em São Borja.
- Open Graph e Twitter Card com imagem de compartilhamento de 1200 x 630.
- Dados estruturados JSON-LD do tipo `AccountingService`, com localização e área atendida.
- `sitemap.xml`, `robots.txt` e `llms.txt` (resumo do escritório para buscadores com IA).
- Nenhuma foto pesada: os visuais do topo e dos serviços são feitos em HTML e CSS, e o ícone é SVG.
- Respeita "reduzir movimento": com a preferência ligada, as animações e os ciclos não rodam e o conteúdo aparece direto.
- Seções com `aria-labelledby`, campo com `aria-invalid` e foco levado para a confirmação do formulário.

## Estrutura

```text
.
├── index.html          # página única: HTML, CSS e JS no mesmo arquivo
├── privacidade.html    # política de privacidade
├── favicon.svg
├── og-image.jpg        # imagem de compartilhamento
├── sitemap.xml
├── robots.txt
├── llms.txt
├── vercel.json         # redirecionamento para o domínio oficial
└── docs/               # prints deste README
```

## Como rodar localmente

Não há dependências. Basta servir a pasta:

```bash
npx serve .
# ou
python -m http.server 8000
```

Depois abra `http://localhost:8000` (ou a porta indicada). O Analytics fica desligado fora do domínio oficial.

## Deploy

Hospedado na Vercel, ligado a este repositório: cada push na `main` publica o site em produção.

---

<sub>Feito por [Matheus Mattos Chaves](https://matheusdev-lovat.vercel.app) · [GitHub](https://github.com/MatheusMattos-Dev)</sub>
