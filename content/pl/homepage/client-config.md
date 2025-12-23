---
title: "Konfiguracja Twojego Minecrafta"
header_menu_title: "Konfiguracja"
navigation_menu_title: "Konfiguracja Minecrafta"
weight: 2
header_menu: true
---
### Podstawowa instalacja

Robimy to jednorazowo na start, i jeśli powiadomię że zmieniamy wersję Forge (co będzie raczej rzadkie).

1. Pobieramy Minecrafta.
2. Odpalamy Launcher, odpalamy grę raz i zamykamy jak się wszystko wczyta (bonus: dajemy dalej jak Narrator zacznie gadać by się zamknął).
3. Pobieramy [Forge 47.4.10](https://maven.minecraftforge.net/net/minecraftforge/forge/1.20.1-47.4.10/forge-1.20.1-47.4.10-installer.jar). 
4. Odpalamy pobrany plik, klikamy OK nic nie zmieniając, i czekamy aż skończy.
5. Odpalamy Minecraft Launcher. Sprawdzamy czy Forge się pojawia normalnie - od teraz zawsze chcemy by tak było (znaczy, jak chcemy zagrać na super duper Ekipowym serwerze, poza tym róbta co chceta).
![Forge in Launcher](/images/forge-in-launcher.png)
6. Odpalamy grę jeszcze raz. Jak launcher da ostrzeżenie, to klikamy by się nie czepiał ponownie. Jak gra się wczyta to zamykamy jeszcze raz i lecimy dalej z ustawianiem.

### Ustawienie RAMu

Dobrze ustawić RAM ile może maszyna wirtualna Javy wykorzystać dla Minecrafta, bo domyślnie to jest jakaś śmieszna ilość.  
Mysimy to zrobić po każdej instalacji Forge (co jak wspomniałem wyżej, powinno być rzadkie).

1. Klikamy na zakładkę instalacji na górze.
![Installations in Launcher](/images/launcher-installations-pl.png)
2. Klikamy na 3 kropki przy instalacji Forge, i dajemy Edit.
![Installations in Launcher](/images/launcher-installations-forge-edit.png)
3. Rozwijamy więcej opcji na dole. 
![Installations in Launcher](/images/launcher-installations-more-options.png)
4. W polu JVM ARGUMENTS na początku mamy takie gówno `-Xmx2G` czy coś takiego. 2G oznacza że Minecraft dostanie max 2GB RAMu. Zmieniamy tą wartość na... no właśnie, to zależy ile macie RAMu na kompie. Oczywiście należy dać trochę mniej niż się ma w sumie by jakiś Discord, przeglądarka itp też mogły działać. Ja lubię dać minimum 10GB - taka ilość generalnie powinna wystarczyć, ale jak macie więcej RAMu dostępnego to możecie dać więcej.
![Installations in Launcher](/images/launcher-installations-ram.png)
5. Klik na Save.

### Mody
To teraz musimy zainstalować mody. Mody powinny się zgadzać z tym co na serwerze, poza modami co jasno zaznaczają że są "client-only" - takie można usuwać, dodawać itd jak się chce.

Dla łatwego startu, zrobiłem zipa z naszymi modami serwerowymi + moimi polecanymi klientowymi. Pobieramy go [klikając tu](https://mega.nz/file/w4dkSaxa#ey8SYpTR0heJGJ8072dqKkJgrdQ8V0rBv4reMzQ7eZc).

Potem odpalamy eksplorer, i w pasku wklepujemy `%appdata%/.minecraft`. Pierw polecam usunąć foldery `mods` i `pointblank` (jeśli istnieją) tak dla spokoju że nic starego nie zostanie - no chyba że coś się doinstalowało samemu, to już wtedy sami się bawcie. I wtedy po prostu rozpakować całą zawartość zipa tutaj, w folder Minecraftowy.

Istnieje możliwość że będziemy raz na jakiś czas coś w modach zmieniać - czy dodać, czy usunąć, czy aktualizować. Ale wtedy dam znać na Discordzie (i wtedy ma głównie znaczenie by te foldery pierw usunąć).

### Shader i Resource packs (opcjonalne, ale polecane)
Mody z paczki pozwalają na użycie shaderów. Możecie sobie pobrać jakie chcecie (tzn jeśli są na Minecrafta 1.20.1 i wspierają Distant Horizons), albo możecie pobrać ode mnie. 

Czemu osobna paczka? A bo shadery można sobie modyfikować wg własnego uznania, a w zipie dałem własne ustawienia.

Możecie pobrać zipa [klikając tu](/dl/shaders-resources-latest.zip?v=2). Tak jak z modami - wywalamy wszystko z paczki do folderu Minecrafta.

### Ustawienia gry

Już prawie, już prawie. Teraz odpalamy Minecrafta ponownie. Jak coś wywali błędy to musicie na mnie krzyczeć, ale zakładamy że nic nie wywali - to mamy kilka rzeczy do ustawienia, więc wchodzimy w **Opcje**.

##### Zasięg Widzenia i Distant Horizons
Pierw chcemy kilka bardzo ważnych zmian. Serwer jest ustawiony tak że i tak nie prześle więcej niż 12 chunków. To jest po to by oszczędzić zasoby serwerowe (bo chcemy tanio, nie?). Ale nie bójta, zasięg widzenia będziemy mieli jeszcze większy niż byśmy mogli normalnie, bo mamy w Modach **Distant Horizons**. Tak więc tak:

1. Pierw wchodzimy w ustawienia Wideło. Tam zmieniamy zarówno zasięg widzenia jak i zasięg symulacji na `12`.
![Render Distance](/images/render-distance.png)
2. Dajemy **Done**.
3. Na głównym ekranie opcji klikamy guzior z takimi kolorowymi kwadratami.
![Distant Horizons Settings Button](/images/dh-settings-button.png)
4. Tutaj chcemy się opewnić że **Enable Rendering** jest ustawione na `True`, **Enable Distant Generation** na `False` (by serwer to robił, nie klient), i że **Render Distance** jest... znacznie większy niż ten minecraftowy. Myślę że `64` do `128` na start będzie ok - w przyszłości może `256`, ale na razie serwer ma problem wygenerować tyle mapy w rozsądnym czasie. Możecie generalnie zmniejszyć zasięg i jakość w ustawieniach jak wam zmula.
![Distant Horizons Settings](/images/dh-settings-128.png)
5. Naturalnie dajemy **Done**.

##### Sterowanie
Dalej. Gramy z Point Blank, a ten mod potrafi błędy w shaderach zrobić jak po raz pierwszy po wczytaniu gry wyjmiemy broń. Na szczęście tylko raz na odpalenie gry, więc możemy się posiłkować wczytaniem shaderów na nowo. By to ułatwić, to polecam wejść w **Controls**, potem **Key Binds**, i w kategorii "Oculus" ustawić keybind dla **Reload Shaders** na coś co się zapamięta - ja sam mam F6 wybrane. Dajemy **Done** i **Done**. Teraz jak wyjmiemy broń i nagle widzimy jaskinie, to wciskamy ten guzior, i pozamiatane póki gry nie wyłączymy.
![Reload Shaders Keybind](/images/reload-shaders-keybind.png)

##### Resource Packs (opcjonalne, ale będzie ładniej wyglądało)
Pierw chcemy włączyć resource packi (jeśli je zainstalowaliśmy). Klikamy w **Resource Packs** i przenosimy kilka na z lewa na prawo klikając na ikonkę, a potem po prawiej zmieniamy kolejność by wyglądało mniej więcej tak jak na skrinie. Jak czegoś brakuje, to czegoś brakuje, trudno. Jak gotowe to klikamy **Done**.
![Resource Packs Selection](/images/resourcepacks-selection.png)

##### Shadery (opcjonalne, ale będzie ZNACZNIE ładniej wyglądało)
Ustawienie na które każdy czekał - shadery.

Wchodzimy w ustawienia grafiki, a tam na górze jest przycisk od paczek shaderów. Wbijamy, i się upewniamy że shadery są włączone, i podświetlone shadery to te z którymi chcemy grać, czy to jakieś własnoręcznie wybrane czy te ode mnie (jeśli są one tylko z zipa ode mnie, to to będzie **ComplementaryUnbound_r5.6.1.zip**).
![Shader Packs Selection](/images/shaders-selection.png)

Jeśli chcemy dostosować shadery, to po wybraniu shadera możemy na dole wbić w jego ustawienia. Jeśli zainstalowaliście ode mnie to dałem tam swoje Customowe ustawienia, które działały u mnie jeszcze na lapku, i generalnie powinno działać git. Ale jak ktoś chce dać lepsze efekty, albo zwiększyć wydajność to można pogrzebać - same shadery mają też kilka domyślnych profili do wybrania, więc jak kto tam woli i jak komu tam to chodzi.

Na koniec naturalnie trzeba klepnąć **Done**.

##### Borderless (opcjonalne, kwestia gustu)
Wchodzimy w ustawienia wideło, znajdujemy tryb fullscreena, ustawiamy na borderless i dajemy **Done**. Tzn to wedle uznania, ale mamy na to moda, to można skorzystać.

##### Reszta ustawień (opcjonalne)
Polecam jeszcze pogrzebać w ustawienia jakości wideo w zależności od preferencji i wydajności. Polecam też m.in. zwiększyć wysokość chmur w **Quality+** - nie pamiętam ile jest domyślne, ja obecnie mam 192 bloków, ale to też generalnie wedle uznania.

To tyle, nie krzyczcie już! Jezu!  
*Tylko notka, że czasem mogę dać znać że coś jest do zmiany, ale wątpię by to było często. Jak coś to dam info na Discordzie.*