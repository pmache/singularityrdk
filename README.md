# Microsoft Singularity RDK — upstream reference archive

> **Status: Reference / Upstream historical source**
>
> To repo nie jest aktywnym projektem portfolio ani kodem autorskim właściciela mirroru. Służy jako historyczna referencja do Microsoft Research Singularity.

## Co to jest

Singularity był projektem badawczym Microsoft Research dotyczącym niezawodnych systemów, języków programowania, izolacji procesów i narzędzi weryfikacyjnych. RDK zawiera materiały źródłowe i kontekst architektoniczny związany z tym systemem.

## Provenance

Oryginalnym źródłem i autorem projektu jest Microsoft Research oraz zespół Singularity. Repo w tym portfolio pełni wyłącznie rolę mirroru/referencji.

Nie należy przypisywać właścicielowi tego repo autorstwa:
- kernela Singularity,
- Software Isolated Processes,
- Channels/Contracts,
- Exchange Heap,
- Bartok/related toolchain concepts,
- pozostałych elementów RDK.

## Relacja z aktywnym projektem

```text
singularityrdk -> historical upstream reference
singularity-os -> original active experimental implementation
```

`singularity-os` może inspirować się koncepcjami Singularity, ale powinien pozostać własną implementacją i dokumentować różnice. To repo nie jest zależnością buildową canonical projektu.

## Do czego służy to repo

- badania architektury oryginalnego Singularity,
- porównywanie terminologii i kontraktów,
- analiza SIP/Channels/Exchange Heap,
- sprawdzanie historycznych decyzji projektowych,
- zachowanie materiału źródłowego do celów edukacyjnych/research.

## Build feasibility

**Status: Historical / environment-specific**

Nie deklarujemy współczesnej buildowalności bez odtworzenia oryginalnego środowiska RDK i weryfikacji pełnego toolchainu.

### Reference Gate SRDK-R1 — Reproduction

**PASS:** istnieje dokładnie udokumentowane środowisko, wersje narzędzi i procedura pozwalająca odtworzyć historyczny build.  
**FAIL:** repo jest opisywane jako współczesny, wspierany system gotowy do builda.

## Licensing / legal

Warunki użycia pochodzą z oryginalnej dystrybucji RDK i plików licencyjnych towarzyszących źródłom. Należy respektować ich treść oraz pochodzenie poszczególnych komponentów.

Repo nie powinno otrzymywać nowej licencji, która sugerowałaby własność całego upstream source tree.

## Maintenance policy

Dozwolone:
- poprawki dokumentacji i provenance,
- indeksowanie materiałów,
- notatki badawcze,
- reprodukcja historycznego środowiska.

Nie dodajemy aktywnej roadmapy produktu ani niezależnych nowych funkcji do RDK. Nowe eksperymenty trafiają do `singularity-os` lub osobnego repo.
