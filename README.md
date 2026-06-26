# KiCad PCB Projects

Repozytorium projektów płytek PCB rysowanych w **KiCad**.

## Struktura

```
KiCad/
├── libraries/                 # wspólne symbole, footprinty (.kicad_sym, .pretty)
├── bipolars/                  # projekt PCB
├── AVR_STM32_communication/
├── .gitignore
└── README.md
```

Nowy projekt dodajesz jako folder z plikami `*.kicad_pro`, `*.kicad_sch`, `*.kicad_pcb`.

## Co jest w repozytorium

- `*.kicad_pro` — plik projektu
- `*.kicad_sch` — schemat
- `*.kicad_pcb` — PCB
- biblioteki w `libraries/` (symbole, footprinty własne)

## Czego nie commitujemy

- `*-backups/` — automatyczne kopie zip
- `*.kicad_prl` — ustawienia widoku (per użytkownik)
- `.history/` — lokalna historia edycji
- `*.lck`, `~*.lck` — pliki blokady (projekt otwarty w KiCad)
- `fp-info-cache` — cache footprintów

## Dodawanie projektu

1. Utwórz folder o nazwie projektu (np. `moja_plytka/`).
2. Umieść tam pliki `.kicad_pro`, `.kicad_sch`, `.kicad_pcb`.
3. Wspólne symbole/footprinty → `libraries/`.

## Gerbery / produkcja

Pliki produkcyjne (Gerber, drill) generuj lokalnie i commituj opcjonalnie w podfolderze `gerber/` danego projektu, gdy zamawiasz płytkę — wtedy masz powiązanie wersji PCB z plikami do fabrykacji.
