# moja-firma-produkcja-uslugowa

**Agent zapytań ofertowych dla polskiej firmy: firma produkcyjno-usługowa.** Czyta zapytanie ofertowe z PDF, znajduje podobne zamknięte projekty z ich prawdziwą marżą, liczy roboczogodziny i sprawdza moce zakładu, a na końcu proponuje, czy wyceniać i na jakich warunkach.

Pakiet branżowy paczki [moja-firma](https://github.com/majchrzycki-com/moja-firma). Procedura w formacie [Agent Skills](https://agentskills.io/specification) (`SKILL.md`) działa w Claude, ChatGPT i Codex, Microsoft 365 Copilot, Gemini oraz OpenClaw.

## Czego agent nie zrobi

Nie poda ceny i nie zaproponuje marży dla nowego tematu. To decyzja handlowca, a przy dużej wartości — zarządu. Agent pokazuje, ile podobne tematy kosztowały naprawdę i czy zakład je udźwignie, żeby ta decyzja zapadła na danych, a nie na optymistycznej pamięci.

Nie zastąpi też porządku w danych. Jeśli koszt rzeczywisty zamkniętych projektów nie jest nigdzie zapisany, agent nie ma na czym liczyć — i to jest najczęstszy powód, dla którego pierwsze podejście do takiego agenta kończy się ładną tabelą z pustą kolumną. W prawdziwej firmie zacznijcie od jednego arkusza z kosztem powykonawczym projektów z ostatniego roku. Dopiero potem agent.

## Wypróbuj na danych ćwiczeniowych

W katalogu [`dane-cwiczeniowe/`](dane-cwiczeniowe/) są fikcyjne dane firmy: `obciazenie.csv`, `obciazenie.xlsx`, `projekty-zamkniete.csv`, `projekty-zamkniete.xlsx`, `zapytanie.pdf`. Pliki XLSX i CSV mają tę samą treść.

1. Zainstaluj procedurę `zapytanie-ofertowe` (niżej).
2. Dodaj pliki ćwiczeniowe do wiedzy agenta albo załącz je do rozmowy.
3. Napisz:

```text
Mamy nowe zapytanie. Przeprowadź analizę według instrukcji projektu, licząc kodem na plikach z wiedzy.
```

4. Porównaj odpowiedź z [WYNIK-KONTROLNY.md](WYNIK-KONTROLNY.md). Jest tam też „krok z rzeczywistością”: jedna zmiana w danych i wynik, który agent powinien po niej pokazać.

## Instalacja

### Claude Code

```text
/plugin marketplace add majchrzycki-com/moja-firma
/plugin install moja-firma-produkcja-uslugowa@moja-firma
```

### Pozostałe narzędzia

```bash
node scripts/build.mjs
```

Skrypt tworzy `dist/skills/` dla Claude, Codex, OpenClaw i Copilot Cowork oraz `dist/instrukcje/` z tekstem do wklejenia w agencie Microsoft 365 Copilot, Gemie albo projekcie ChatGPT. Szczegóły instalacji w każdym narzędziu: [README rdzenia moja-firma](https://github.com/majchrzycki-com/moja-firma#instalacja).

## Ten sam agent krok po kroku

- [Agent zapytań ofertowych w Claude](https://majchrzycki.com/blog/agent-zapytan-w-claude-krok-po-kroku?utm_source=github&utm_medium=referral&utm_campaign=moja-firma&utm_content=zapytanie-ofertowe)
- [Agent zapytań ofertowych w Microsoft 365 Copilot](https://majchrzycki.com/blog/agent-zapytan-w-microsoft-365-copilot-krok-po-kroku?utm_source=github&utm_medium=referral&utm_campaign=moja-firma&utm_content=zapytanie-ofertowe)
- [Agent zapytań ofertowych w ChatGPT](https://majchrzycki.com/blog/agent-zapytan-w-chatgpt-krok-po-kroku?utm_source=github&utm_medium=referral&utm_campaign=moja-firma&utm_content=zapytanie-ofertowe)
- [Agent zapytań ofertowych w Gemini](https://majchrzycki.com/blog/agent-zapytan-w-gemini-krok-po-kroku?utm_source=github&utm_medium=referral&utm_campaign=moja-firma&utm_content=zapytanie-ofertowe)

Gdzie ten agent mieści się w całej firmie i jakich jeszcze agentów potrzebuje firma produkcyjno-usługowa: [darmowy poradnik branżowy](https://majchrzycki.com/transformacja-agenci-ai/firma-produkcyjno-uslugowa?utm_source=github&utm_medium=referral&utm_campaign=moja-firma&utm_content=zapytanie-ofertowe#pobierz).

## Na własnych danych

Zacznij od procedury `kontrola-danych` z rdzenia moja-firma na eksporcie z Waszego programu. Jeśli kolumny nazywają się inaczej, agent pokaże przypisanie i poprosi o potwierdzenie. Pierwszy tydzień puść agenta obok normalnej pracy jednej osoby i porównuj wyniki.

Procedura nie jest poradą prawną, podatkową ani handlową. Wynik sprawdza osoba, która za niego odpowiada.

## Licencja

[MIT](LICENSE), dla procedur, skryptów i danych ćwiczeniowych.

Autor: [Krzysztof Majchrzycki](https://majchrzycki.com/o-mnie?utm_source=github&utm_medium=referral&utm_campaign=moja-firma&utm_content=zapytanie-ofertowe), wdrożenia AI w polskich firmach.

---

**English:** moja-firma-produkcja-uslugowa is an industry pack of the open [moja-firma](https://github.com/majchrzycki-com/moja-firma) Agent Skills for Polish SMBs. It contains one `SKILL.md` procedure (in Polish), fictional practice data and expected results. MIT licence.
