# KEGA Projekt - Laboratórium aplikovaných technológií umelej inteligencie

## Zameranie projektu
Projekt sa zameriava na vybudovanie moderného laboratória aplikovaných technológií umelej
inteligencie pre priemysel. Laboratórium bude pozostávať z 5 rôznych pracovísk zameraných na
spracovanie obrazu, videa a zvuku pre priemyselné aplikácie. Pracoviská sú navrhnuté tak, aby mohli
byť nezávislé od operačného systému (Linux, Windows) a softvéru pre HNS (Matlab, Python, ...).
Laboratórium budú využívať študenti 3. ročníka bakalárskeho štúdia a študenti 1. a 2. ročníka
inžinierskeho štúdia na vybraných predmetoch a študenti bakalárskych, diplomových, individuálnych
a tímových prác, ale aj doktorandi. Plánujeme nasledovné pracoviská:

## Pracovisko 2 - HMI aplikácie pomocou hlbokých neurónových sietí
Počítačová zostava s výkonnou grafickou kartou, kvalitná hĺbková kamera, priemyselný
riadiaci systém, existujúci riadiaci systém a existujúci model CNC. HMI pracovisko pre
rozpoznávanie gest, tváre, hlasových povelov pomocou hlbokých neurónových sietí.

### Rozpoznávanie hlasových povelov pomocou hlbokých neurónových sietí.
Rozpoznávanie hlasových povelov predstavuje jednu z praktických aplikácií spracovania rečového signálu a metód umelej inteligencie. 
Cieľom je automaticky identifikovať krátke hovorené povely, napríklad „štart“, „stop“, „zapni“ alebo „dopredu“, a zaradiť ich do vopred definovaných tried. 
Takéto systémy nachádzajú uplatnenie pri hlasovom ovládaní zariadení, robotov, inteligentných domácností alebo pri interakcii človeka so strojom (HMI).
![princip hlas povely](image/hlasove_povely_princip.png)
Obr.1 Principiálna schéma rozpoznávania hlasových povelov

Moderné riešenia využívajú najmä hlboké neurónové siete, ktoré dokážu z audio signálu automaticky extrahovať charakteristické príznaky a následne vykonať klasifikáciu povelu. 
Vstupný zvukový signál sa môže spracovávať priamo vo formáte RAW signálu alebo sa najskôr transformuje do vhodnej časovo-frekvenčnej reprezentácie, napríklad Mel-spektrogramu. [Spektrogram_postup](document/spektogram.pdf)
![ukazka_spectrogram](image/right.png)
Obr.2 Ukážka RAW signálu a spektrogramu hlasového povelu „right“

#### Dataset hlasových povelov (wav formát):
[Speech_commands_v0.02](https://www.kaggle.com/datasets/mok0na/speech-commands-v002)


#### Použité modely:
Na klasifikáciu sa následne používajú napríklad konvolučné neurónové siete (CNN), rekurentné siete ako LSTM a GRU, kombinované modely napr. CNN+LSTM  alebo modernejšie architektúry založené na mechanizme attention.
![ukazka_1DCNN](image/hlasove_povely_1DCNN.png)
Obr.3 Príklad rozpoznávania hlasového povelu pomocou RAW signálu a CNN s 1D konvolúciou

Úlohou je vytvoriť a overiť rôzne architektúry hlbokých neurónových sietí a ich schopnosť spoľahlivo rozpoznávať vybranú množinu hlasových povelov a vyhodnotiť ich úspešnosť a iných klasifikačných metrík na testovacích zvukových záznamoch.

Návod na trénovanie a testovanie vybraných architektúr HNS (RAW+1D-CNN, RAW+CNN-LSTM, SPECT+CNN)

[Návod_Hlasové_povely](document/guide_hlas_povely.pdf)

Dosiahnuté výsledky:
- G. Bogi, Rozpoznávanie hlasových povelov pomocou konvolučných sietí, DP, FEI STU, 2021, [Vysledky_DP_Bogi](document/vysledky_dp_bogi.pdf)
- Berki, Lúčny, Rozpoznávanie hlasových povelov, Projekt HNS, 2023, [Vysledky_HNS_Projekt_Berki_Lúčny](document/Klasifikacia_hlasovych_povelov_Berki.pdf)
- Stoliar, Lobach, Rozpoznávanie hlasových povelov, Projekt HNS, 2025, [Vysledky_HNS_Projekt_Stoliar_Lobach](document/Klasifikacia_hlasovych_povelov_Stoliar.pdf)



### Rozpoznávanie správne nasadeného rúška pomocou hlbokých neurónových sietí.
Rozpoznávanie správne nasadeného ochranného rúška predstavuje jednu z praktických úloh počítačového videnia, pri ktorej je možné využiť metódy hlbokého učenia. 
Cieľom je na základe obrazu alebo videozáznamu automaticky detegovať osoby a následne určiť, či majú rúško nasadené správne, nesprávne alebo ho nemajú vôbec. 
![princip mask detect](image/mask_recognition_princip.png)
Obr.4 Principiálna schéma rozpoznávania správneho nasadenia rúška

Na riešenie tejto úlohy sa využívajú najmä konvolučné neurónové siete (CNN) a moderné modely na detekciu objektov, 
napríklad rodina YOLO, ktoré umožňujú lokalizovať tvár alebo osobu v obraze a zároveň vykonať klasifikáciu spôsobu nasadenia rúška.

### Rozpoznávanie statických gest ruky pomocou hlbokých neurónových sietí.
Rozpoznávanie gest ruky predstavuje významnú oblasť počítačového videnia, ktorá umožňuje prirodzenú a bezkontaktnú komunikáciu človeka s počítačom, robotom alebo iným technickým zariadením. 
Uplatnenie nachádza napríklad pri ovládaní robotických systémov, v inteligentných domácnostiach, automobiloch alebo pri tvorbe používateľských rozhraní. 
Cieľom je na základe obrazu z kamery automaticky detegovať ruku a následne rozpoznať (klasifikovať) ukazované gesto. 
![princip hand detect](image/gesta_recognition_princip.png)
Obr.5 Principiálna schéma rozpoznávania statických gest ruky

Na automatické rozpoznávanie gest je možné efektívne využiť konvolučné neurónové siete (CNN), ktoré dokážu priamo z obrazových dát extrahovať charakteristické príznaky a následne klasifikovať jednotlivé gestá. 
Vstupný obraz získaný kamerou sa predspracuje, lokalizuje sa oblasť ruky a následne sa pomocou CNN priradí k jednej z definovaných tried gest.

### Rozpoznávanie gest a stavov tváre pomocou hlbokých neurónových sietí.
Rozpoznávanie gest a stavov tváre predstavuje významnú oblasť počítačového videnia zameranú na automatickú analýzu vizuálnych prejavov človeka. 
Okrem identifikácie osoby je možné z obrazu tváre určovať napríklad natočenie a polohu hlavy, prítomnosť okuliarov, otvorenie alebo zatvorenie očí a úst či základné emócie, ako sú úsmev, prekvapenie alebo smútok. 
Takéto systémy nachádzajú uplatnenie pri interakcii človeka s počítačom a robotom, monitorovaní pozornosti vodiča, asistenčných systémoch alebo inteligentných používateľských rozhraniach. 
 
![princip hlava detect](image/tvar_recognition_princip.png)
Obr.6 Principiálna schéma rozpoznávania gest a stavov tváre

Na riešenie týchto úloh je možné efektívne využiť konvolučné neurónové siete (CNN). 
Po detekcii a lokalizácii tváre v obraze CNN automaticky extrahuje charakteristické vizuálne príznaky a na ich základe vykoná klasifikáciu požadovaného stavu alebo regresný odhad, napríklad uhlov natočenia hlavy. 

