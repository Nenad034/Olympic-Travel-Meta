# Olympic Travel — automatizacija objava (Facebook / Instagram)

Interna aplikacija koja od aktuelne ponude Olympic Travel-a pravi gotovu objavu za Facebook i
Instagram; zaposleni je pregleda i odobri, aplikacija je objavi u zakazano vreme i posle par
dana upiše rezultate.

**Stanje:** specifikacija i predlog arhitekture. Koda još nema.

## Dokumenti

| Fajl | Šta je unutra |
| :--- | :--- |
| [Olympic Travel — aplikacija za automatizaciju objava.md](Olympic%20Travel%20%E2%80%94%20aplikacija%20za%20automatizaciju%20objava.md) | **Šta se gradi i zašto** — cilj i obim, kako proces izgleda danas, tok rada, AI sloj, Meta API, faze, rizici i troškovi, sledeći koraci |
| [ARHITEKTURA-Olympic-Travel-Meta-app.md](ARHITEKTURA-Olympic-Travel-Meta-app.md) | **Kako se gradi** — model podataka, slojevi, adapteri, red poslova, ekrani panela, infrastruktura, fazni plan sa izlaznim kriterijumima |

## Ukratko

- Nijedna objava ne ide javno bez potvrde čoveka (`approved_by` je uvek čovek, nikad AI).
- Cena i termin se ne kucaju i ne generišu — dolaze iz izvora i upisuju se programski.
- Predložen stek: NestJS + Prisma + PostgreSQL (API), Next.js (panel) — isti kao Terminal Travel,
  odakle se preuzima deo koda (modul M12 Marketing, M15 AI, M17 panel).

## Šta čeka odluku

Spisak je na kraju oba dokumenta (poglavlje „Sledeći koraci" i „Odluke koje traže vlasnika"):
poddomen i server, ko odobrava objave, link na Instagramu, AI vizuali, pitanja za NeoLab,
izbor 20–30 dosadašnjih objava kao osnova stila.
