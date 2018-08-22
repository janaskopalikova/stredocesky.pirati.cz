# Pirátský web Stredočeského kraje - stredocesky.pirati.cz

* pokud je to možné, je lepší použít Markdown (.md) formát než html
* pokud kód nemůžete otestovat na lokále (stažení celého repa, build a spuštění v jekyllu), dělejte jen drobné změny, kterým rozumíte
* obecně k pirátským šablonám: https://github.com/pirati-web/example.pirati.cz
* další repository pro inspiraci: https://github.com/pirati-web
* technická diskuze (nejen) k webu viz https://chat.pirati.cz/channel/stredocesi (pozor pro přihlášení nesmíte na první stránce nic vyplňovat - ani username ani heslo - a kliknout na bílý nápis na modrém podkladu "Přihlášení pomocí pirátské identity"!)

# Co má nebo musí mít článek

* jméno článku rozumné délky
* autora
* datum (pokud nemá být aktuální)
* titulní fotografii (zobrazuje se v seznamu článků a také v samotném článku nahoře - bez dalšího popisu)
* tagy
* první část textu vhodnou pro automaticky generovaný perex
* text co nejméně formátovaný, bez obtékání obrázků
* možné doplnit více obrázky
* citace v samostatném odstavci s uvozovkama + uvozením autora (před nebo poté)
* dlouhé URL odkazy v seznamu dalších zdrojů je třeba opatřit jednoznačným jménem/popisem (např. iDnes: K Jirkovi se vrátit nechci, říká Andrea Pomeje)

Všechny články jdou přes Jirku Snížka, který ve spolupráci s PKD a mediálním odborem kraje posuzuje, zda patří na krajský web.

# Co má nebo musí mít osobní profilová stránka

* jméno a příjmení, tituly
* u piráta uživatelské uid
* kontakt (minimálně pirátský e-mail), případně linky na osobní weby atd.
* fotka (hlava) - ořezává se do čtverce a nechává se v co nejvyšším rozlišení
* historie vč. data a místa narození, profese a záliby

# Markdown formát

```
# Nadpis
## Menší nadpis
*kurzíva* **tučné písmo** ~~škrtance~~ `kód`
* seznam nečíslovaný
1. seznam číslovaný
[odkaz](http://www.pirati.cz)
obrazek: {% asset 'posts/clanek-jmeno_souboru.jpg' alt='Popis obrázku' %}
```

Jak správně citovat:

```
> „Tohle říkám."
říká Petr Novák.
```

Více viz https://en.wikipedia.org/wiki/Markdown nebo https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

# Jednoduchá editace souborů přímo na githubu

Pro editaci stačí mít github účet, nejsou potřeba žádná speciální práva. Postup je následující:

Pro jednoduché editace je možné použít odkazy "Navrhni úpravu" vpravo dole na každé stránce webu. Odkaz vás přesměruje na přímo na editaci na githugu.
Nebo po rozkliknutí konkrétního souboru na githubu lze kliknout na ikonu tužky v pravém horním rohu (po najetí myší se objeví hláška: "Edit the file in your fork of this project").

1. Změňte potřebné části souboru (nahoře na liště mód "Edit file"),
2. zkontrolujte správnost provedených změn kliknutím na "Preview changes" na horní liště (červeně jsou označeny odebrané části textu, zeleně naopak ty přidané),
3. sjeďte na konec stránky k tabulce "Propose file change" a vyplňte pole "Add an optional extended description..." - stručně a jasně shrňte své změny,
4. klikněte na zelené tlačítko "Propose file change",
5. objeví se nová stránka, kde ještě jednou uvidíte provedené změny a pokud je vše v pořádku, klikněte na horní zelené tlačítko "Create pull request" a pak ještě jednou u druhé tabulky,
6. počkejte, až vaše změny potvdí administrátor stránek (přijde vám do e-mailu zpráva, když se tak stane),
7. a máte HOTOVO!


# Pro linuxáky

Vystačíte si s jakýmkoliv editorem a "git" klientem (balík by se měl jmenovat stejně). Pár tipů pro command line git klienta viz níže - i tak byste ale měli vědět, co v každém kroku děláte!

Více viz https://help.github.com/


## Start

```
mkdir ~/git
cd ~/git
git clone https://github.com/pirati-web/stredocesky.pirati.cz
git config user.name "vas_github_user"
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=3600'
```

## Zápis změn do lokálního repository a přenos na server

```
git status
git add -A
git commit -a
git push
```

## Aktualizace lokálního repository

To udělejte vždy, než něco začnete měnit.

```
git fetch
```
