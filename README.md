# Microsoft Singularity RDK — upstream reference archive

> **Status: Reference / Historical upstream / CODE REVIEWED**
>
> To repo nie jest aktywnym projektem portfolio ani kodem autorskim właściciela mirroru. Służy jako historyczna referencja do Microsoft Research Singularity.

## Co to jest za projekt

Repo zawiera historyczny Microsoft Singularity RDK 2.0: źródła, dokumentację, materiały buildowe i oryginalne pliki licencyjne. Nie jest to nowa implementacja ani fork rozwijany produktowo.

## Do czego służy

- badania architektury oryginalnego Singularity,
- porównywanie SIP/Channels/Contracts/Exchange Heap,
- analiza historycznych decyzji projektowych,
- reprodukcja oryginalnego środowiska badawczego,
- reference source dla clean-room/original experiments w `singularity-os`.

## Stan projektu

**Status: Reference / Historical upstream / CODE REVIEWED**

Source audit potwierdził, że repo jest pełnym historycznym upstream tree, a nie małym własnym patchsetem. Zawiera m.in. `SOURCE/base`, projekty `.csproj/.sg`, dokumenty RDK i historyczne materiały developerskie.

Najważniejszy znaleziony problem dotyczył provenance: root `LICENSE` deklarował zwykły MIT z `Copyright (c) 2020 Me`, co mogło sugerować blanket relicensing całego upstream RDK. Został zastąpiony neutralnym licensing notice wskazującym na oryginalne warunki RDK w `SOURCE/Singularity RDK 2.0 License.pdf` i component-specific notices.

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
       │
       └── concepts/reference only
                ▼
         singularity-os -> canonical original active implementation

singularityos -> older/superseded experimental line
```

`singularity-os` powinien pozostać własną implementacją i dokumentować różnice. To repo nie jest zależnością buildową canonical projektu i nie powinno być kopiowane wholesale do aktywnej linii bez sprawdzenia licencji/provenance.

## Build feasibility

**Status: Historical / environment-specific / verification required**

Nie deklarujemy współczesnej buildowalności bez odtworzenia oryginalnego środowiska RDK i weryfikacji pełnego toolchainu.

### Reference Gate SRDK-R1 — Reproduction

**PASS:** dokładnie opisane wersje narzędzi i środowiska pozwalają odtworzyć historyczny build w izolowanej VM.  
**FAIL:** samo posiadanie source tree jest traktowane jako dowód współczesnego build PASS.

### Reference Gate SRDK-R2 — Provenance

**Stan:** PASS dla repo-level attribution

**PASS:** root dokumentacja jasno mówi, że tree pochodzi z Microsoft Research, a root notice nie próbuje relicencjonować całego upstreamu.  
**FAIL:** repo sugeruje autorstwo właściciela mirroru lub blanket MIT/BSD dla całego RDK.

### Reference Gate SRDK-R3 — Canonical isolation

**Stan:** PASS

**PASS:** `singularity-os` nie wymaga tego tree do builda i korzysta z niego jedynie jako research/reference.  
**FAIL:** aktywny projekt zaczyna zależeć od skopiowanych upstream komponentów bez jawnej analizy licencji i architektury.

## Licensing / legal

Warunki użycia poszczególnych materiałów pochodzą z oryginalnej dystrybucji RDK i component-specific notices. Root `LICENSE` jest teraz wyłącznie provenance/licensing notice i nie stanowi nowego grantu praw do upstream source tree.

## Maintenance policy

Dozwolone:
- poprawki dokumentacji i provenance,
- indeksowanie materiałów,
- notatki badawcze,
- reprodukcja historycznego środowiska.

Nie rozwijamy tego jako nowego produktu. Nowe eksperymenty trafiają do `singularity-os` lub osobnego clean-room repo.
