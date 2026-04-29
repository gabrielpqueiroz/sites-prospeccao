# PRD — Fábrica de Landing Pages para Prospecção

## Objetivo

Sistema de geração rápida de landing pages profissionais para novos clientes. O fluxo é simples: você fornece as informações do cliente, e a IA gera uma landing page completa e pronta para publicar.

---

## Problema

Criar landing pages do zero para cada cliente consome tempo e repete trabalho manual. É necessário um processo padronizado que mantenha qualidade visual alta e permita personalização rápida.

---

## Solução

Um projeto-base com templates prontos + skill de design (UI/UX Pro Max) integrada ao Claude Code. Para cada novo cliente, basta passar o briefing e receber o HTML final personalizado.

---

## Fluxo de Trabalho

```
1. Você informa os dados do cliente (briefing)
2. Claude gera o design system personalizado (cores, fontes, estilo)
3. Claude cria a landing page a partir do template
4. Arquivo salvo em: clientes/[NOME_CLIENTE]/index.html
5. Pronto para publicar
```

---

## Briefing do Cliente (informações necessárias)

Para gerar uma landing page, forneça:

| Campo | Exemplo |
|---|---|
| Nome do profissional/empresa | Dr. João Silva |
| Especialidade / segmento | Ortopedista |
| Público-alvo | Adultos com dores articulares |
| Serviços oferecidos (3-6) | Consulta, Cirurgia, Fisioterapia... |
| Depoimentos reais (opcional) | Nomes + textos |
| Telefone / WhatsApp | 11 99999-9999 |
| Endereço | Rua X, 123 - São Paulo |
| E-mail | contato@clinica.com |
| Instagram / redes sociais | @drjoaosilva |
| Foto do profissional (URL ou arquivo) | — |
| Estilo visual preferido | Moderno / Clássico / Minimalista |
| Cores da marca (opcional) | Azul e dourado |
| Número de anos de experiência | 15 anos |
| Estatística destaque | +3.000 pacientes |

---

## Template Base

- **Localização:** `templates/template-piloto/index.html`
- **Tecnologia:** HTML puro (sem dependências externas além de Google Fonts)
- **Seções:** Hero → Trust Bar → Sobre → Serviços → Depoimentos → Contato → Footer
- **Features:** Responsivo, animações de scroll, menu mobile, botão WhatsApp flutuante, parallax suave
- **Design:** Navy + Gold, tipografia Cormorant Garamond + DM Sans — voltado para profissionais de saúde e serviços premium

---

## Estrutura de Pastas

```
SITES PROSPECCAO/
├── PRD.md                          ← este arquivo
├── templates/
│   └── template-piloto/
│       └── index.html              ← template base
└── clientes/
    └── [NOME_CLIENTE]/
        └── index.html              ← landing page gerada
```

---

## Placeholders do Template

Todos os campos variáveis usam o padrão `[CAMPO]`:

- `[NOME_PROFISSIONAL]` — nome completo
- `[ESPECIALIDADE]` — especialidade ou segmento
- `[TELEFONE]` — número sem formatação (ex: 11999999999)
- `[EMAIL]` — e-mail de contato
- `[ENDERECO]` — endereço completo
- `[FORMACAO]` — formação acadêmica
- `[ESPECIALIZACAO]` — pós-graduação / especialização
- `[SERVICO_1..6]` — nome de cada serviço
- `[DESCRICAO_SERVICO_1..6]` — descrição curta de cada serviço

---

## Critérios de Qualidade

- [ ] Mobile-first, funcional em telas de 320px a 1440px+
- [ ] Botão WhatsApp com link correto e mensagem pré-preenchida
- [ ] Imagens do Unsplash condizentes com o segmento do cliente
- [ ] Design system coerente (cores, fontes e tom alinhados ao cliente)
- [ ] Sem placeholder `[CAMPO]` visível na versão final
- [ ] HTML válido, sem erros de console

---

## Escopo Fora do Projeto

- Hospedagem e publicação (responsabilidade do cliente)
- Domínio e DNS
- Backend / formulários funcionais
- SEO avançado
- Analytics e pixels de rastreamento (adicionados sob demanda)
