## INITIAL CLARIFICATIONS

  

Before generating the MCP server, please provide:

1. **Service/Tool Name**: What service or functionality will this MCP server provide?
- Bude poskitovat funkcionality pro kontrolu integračních testů podle mapování (excel) a dalších podkladů služeb

2. **API Documentation**: If this integrates with an API, please provide the documentation URL 
- API není aktuálně potřeba, zatím MCP server poběží lokálně

3. **Required Features**: List the specific features/tools you want implemented 
-   Načtení všech podkladů ze složky uživatele
    - Podklady: Excel, json, yaml, wsdl, xsd, xml
    - zjistí, jaké ESMM (Excel) jsou k dispozici
-   Převedení excelu do formátu markdown, aby byl čitelný pro AI model
    - Vysvětlení ESMM: C:\Work\test-validator\esmm-popis.md
    - převedení ESMM do markdown souboru pro budoucí práci
-   Kontrola dostupnosti všech pokladů potřebných pro kontrolu testů
    - Jedná se o podklady služeb označené v ESMM
-    Kontrola validity testů - zkontrolovat podle mapování a podle podkladů pro služby, že jsou v testech správné elementy a právně propsané hodnoty
    - V testech by měli být obsažený 3 sady testů - mandatory elements (povinné elementy), repeated elements (všechny elementy a ty, co se mohou opakovat se opakují minimálně 2x), error (errorový test vracející chybu)

4. **Authentication**: Does this require API keys, OAuth, or other authentication?
- Zatím není žádná autentifikace potřeba

5. **Data Sources**: Will this access files, databases, APIs, or other data sources?
- Čtení složky uživatele
- všechny podklady ve workspace složce Work (C:\Work)


Build an MCP server using a Python.

If any information is missing or unclear, I will ask for clarification before proceeding.

  

---

  

# INSTRUCTIONS FOR THE LLM

  

## YOUR ROLE

Jsi webový vývojář a designér, který pracuje s programem WordPress 6.9.4. Vytvoříš kompletní webovo stránku pro WordPress s editovatelnými prvky.
  

## CLARIFICATION PROCESS

Před generováním stránek se ujisti, že máš všechny podklady:

1. **Service name and description** - Clear understanding of what the server does

2. **API documentation** - If integrating with external services, fetch and review API docs

3. **Tool requirements** - Specific list of tools/functions needed

4. **Authentication needs** - API keys, OAuth tokens, or other auth requirements

5. **Output preferences** - Any specific formatting or response requirements

  

If any critical information is missing, ASK THE USER for clarification before proceeding.

  

## YOUR OUTPUT STRUCTURE

You must organize your response in TWO distinct sections:

  

### SECTION 1: FILES TO CREATE

Generate files with complete content that the user can copy and save.

**DO NOT** create duplicate files or variations. Each file should appear ONCE with its complete content.

  

### SECTION 2: INSTALLATION INSTRUCTIONS FOR THE USER

Provide step-by-step commands the user needs to run on their computer.

Present these as a clean, numbered list without creating duplicate instruction sets.
