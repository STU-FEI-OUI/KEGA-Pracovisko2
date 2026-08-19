# KEGA Projekt - Laboratórium aplikovaných technológií umelej inteligencie

## Anotácia projektu
Umelá inteligencia (UI) je technológia, ktorá dokáže simulovať ľudské uvažovanie a učenie
pomocou algoritmov strojového učenia a hlbokých neurónových sietí (HNS). V dnešnej dobe sa
UI stala neoddeliteľnou súčasťou mnohých oblastí nášho života ako napr. zdravotníctvo, doprava,
priemysel, spracovanie textu, atď. V zdravotníctve sa používa napríklad na diagnostiku a predikciu
chorôb na základe analýzy obrazových a laboratórnych výsledkov. V doprave sa používa na
plánovanie trás, predikciu a minimalizáciu meškaní a optimalizáciu spotreby paliva. V priemysle sa
používa na optimalizáciu výrobných procesov a znižovanie nákladov, hodnotenie kvality produktov,
atď. Oblasť spracovania textu zahŕňa analýzu, porozumenie a generovanie textu.

Dnešné programovateľné logické automaty (PLC – programmable logic controller; PAC –
programmable automation controller) majú za sebou štyridsať rokov vývoja. Ide o priemyselné
riadiace systémy schopné riadiť a monitorovať spojité (tlaky, teploty, prietoky, ...) a diskrétne
udalostné systémy (dopravníky, roboty, ...). Trend vývoja programovacích jazykov PLC spôsobil
rozšírenie základných bitových inštrukcií o nové (matematické, komunikačné, diagnostické, riadiace,
bezpečnostné, ...). Významný posun nastal aj v oblasti výkonu procesorov (CPU) PLC. Uvedené
zmeny umožňujú nasadenie metód UI pre riadenie a monitorovanie procesov. Existujú dva prístupy
implementácie UI v PLC, implementácia v CPU alebo v externom zariadení (PC, priemyselné PC,
Edge zariadenie, cloud, ...).

## Zameranie projektu
Projekt sa zameriava na vybudovanie moderného laboratória aplikovaných technológií umelej
inteligencie pre priemysel. Laboratórium bude pozostávať z 5 rôznych pracovísk zameraných na
spracovanie obrazu, videa a zvuku pre priemyselné aplikácie. Pracoviská sú navrhnuté tak, aby mohli
byť nezávislé od operačného systému (Linux, Windows) a softvéru pre HNS (Matlab, Python, ...).
Laboratórium budú využívať študenti 3. ročníka bakalárskeho štúdia a študenti 1. a 2. ročníka
inžinierskeho štúdia na vybraných predmetoch a študenti bakalárskych, diplomových, individuálnych
a tímových prác, ale aj doktorandi. Plánujeme nasledovné pracoviská:

### Pracovisko 1.
Počítačová zostava s výkonnou grafickou kartou, kvalitná hĺbková kamera, priemyselný
riadiaci systém, model. Cieľom pracoviska bude spracovanie obrazu na kontrolu kvality objektov
(výrobkov).

### Pracovisko 2. 
Počítačová zostava s výkonnou grafickou kartou, kvalitná hĺbková kamera, priemyselný
riadiaci systém, existujúci riadiaci systém a existujúci model CNC. HMI pracovisko pre
rozpoznávanie gest, tváre, hlasových povelov pomocou hlbokých neurónových sietí.

### Pracovisko 3.
Počítačová zostava s výkonnou grafickou kartou, kvalitná hĺbková kamera, Nvidia Jetson
(Edge zariadenie), priemyselný riadiaci systém, existujúci robot (UR). Pracovisko pre detekciu
objektov pomocou hlbokého učenia vhodné napr. pre účely bin picking, pick & place.

### Pracovisko 4. 
Počítačová zostava, kvalitná kamera, Nvidia Jetson (Edge zariadenie), priemyselný riadiaci
systém. Cieľom pracoviska bude sledovanie pohybujúcich sa objektov na videu pomocou hlbokých
neurónových sietí.

### Pracovisko 5. 
Počítačová zostava, kvalitný mikrofón, Nvidia Jetson (Edge zariadenie), priemyselný
riadiaci systém. Cieľom pracoviska bude spracovanie zvuku a odoslanie výsledku spracovania do
priemyselného riadiaceho systému s cieľom učenia kvality.