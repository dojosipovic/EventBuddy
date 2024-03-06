# Event Buddy

## Projektni tim

Ime i prezime | E-mail adresa (FOI) | JMBAG | Github korisničko ime
------------  | ------------------- | ----- | ---------------------
Dominik Josipović | djosipovi21@foi.hr | - | djosipovi21
Sebastijan Vinko | svinko21@foi.hr | - | svinko21
Karlo Mikec | kmikec20@foi.hr | - | kmikec20

## Opis domene
Projekt pokriva domenu upravljanja administracijom aplikacije o budućim događajima (koncerti, seminari, radionice...). Aplikacija radi tako da organizator događaja objavi događaj u aplikaciji na mobitelu tako da popuni obrazac u koje upisuje osnovne informacije o događaju (naziv, kratak opis, mjesto, vrijeme, broj mogućih sudionika). Korisnici mogu vidjeti događaje koje je kreirao organizator te se mogu pretplatiti na događaj i tako zauzeti svoje mjesto na događaju.
U sustavu će biti još uloge "Moderator" i "Administrator". Moderator će moći upravljati događajima koje je bilo koji organizator kreirao na način da ih može sakriti ukoliko primijeti da objavljeni događaj nije prikladan za zajednicu. Organizatorima može biti oduzeta uloga od strane moderatora ako prekrši pravila zajednice objavljivanjem neprikladnih događaja. Moderator može dodati ulogu organizatora korisniku za kojeg se utvrdi da je pouzdana i ovlaštena osoba za organiziranje događaja, takav korisnik mora poslati zahtjev u aplikaciji ma mobitelu da želi postati organizator, a moderator ih treba odobriti ili odbiti u desktop aplikaciji. Uloga administratora ima sve ovlasti moderatora i organizatora, ali može mijenjati podatke na svakom kreiranom događaju. Administrator može i obrisati događaj (tako da više ne postoji u aplikaciji) Administrator i organizator mogu kreirati svoje događaje i pretplatiti se na tuđe, ali putem mobilne aplikacije. Administratoru i moderatoru će biti omogućene navedene ovlasti pristupom sustavu preko desktop aplikacije koja je namijenjena za administraciju dok običan korisnik ili organizator neće moći pristupiti aplikaciji preko desktop verzije, nego će morati pristupiti preko mobilne verzije.

## Specifikacija projekta

Oznaka | Naziv | Kratki opis | Odgovorni član tima
------ | ----- | ----------- | -------------------
F01 | Upravljanje korisničkim računom | Korisnik se prijavljuje u aplikaciju na način da unosi svoje korisničko ime i lozinku. Korisnik na svojem profilu u aplikaciji može mijenjati lozinku. Lozinka se mijenja na način da se upisuje stara lozinka te se dva puta upisuje nova lozinka kao što je to slučaj kod registracije. | Karlo Mikec
F02 | Pregledavanje događaja | Korisnik može pregledavati događaje koji su kreirani te ima opcije pretraživanja i filtriranja događaja. Događaji mogu biti pretraženi prema naslovu te biti filtrirani prema datumu odvijanja, vremenu početka i završetka te mjestu. | Dominik Josipović
F03 | Upravljanje događajem | Korisnik može pregledavati korisnike koji su se pretplatili na događaj i ukoliko želi, može određene korisnike maknuti s liste ili čak zabraniti pristup događaju. Postoji opcija otkazivanja događaja ukoliko se utvrdi da se događaj iz određenog razloga ne može izvoditi (opcija obustavi događaj). | Dominik Josipović
F04 | Nadziranje zajednice | Korisnik će moći prilikom pregledavanja događaja sakriti događaj ukoliko utvrdi da je događaj neprikladan ili nekim slučajem krši pravila zajednice (opcija sakrij događaj). Skriveni događaj neće se vidjeti u aplikaciji niti će korisnici dobivati nikakve obavijesti o njemu, također organizator događaja neće vidjeti svoj događaj. Organizator dobiva prvo upozorenje o kršenju pravila, a sljedeće upozorenje oduzima mu ulogu organizatora. Ukoliko moderator utvrdi da organizator ne zaslužuje svoju ulogu, ima ovlasti odmah mu maknuti ulogu organizatora pri čemu postaje običan korisnik. | Sebastijan Vinko
F05 | Izmjena podataka događaja | Administrator, uz to što ima iste ovlasti kao i moderator, još može napraviti sve izmjene na tuđim događajima kao što može organizator na svojem. Administrator može izmijeniti podatke događaja. Može izmjeniti naziv, opis, vrijeme događaja te mjesto održavanja događaja. Također administrator može trajno maknuti događaj iz aplikacije (opcija brisanje događaja). | Dominik Josipović
F06 | Upravljanje korisnicima i zahtjevima | Administrator može bilo kojem korisniku dodijeliti ulogu organizatora i moderatora te iste oduzeti. Korisnik postaje organizatorom ukoliko pošalje zahtjev da želi postati organizator te mu tada administrator ili moderator mora odobriti zahtjev nakon čega se korisniku dodjeljuje uloga organizatora. Moderator i administrator će moći vidjeti zahtjeve korisnika da postanu organizatori. Za svakog korisnika vidjeti će jedan zahtjev na kojeg mogu kliknuti te vidjeti detalje upita korisnika. Moguće je odobriti zahtjev klikom na gumb "Odobri" ili "Odbij". Ulogu moderatora korisnik dobije na način da mu je dodijeli administrator. Moderator može organizatoru oduzeti ulogu. Korisnički račun može u isto vrijeme biti i moderator i organizator.	| Sebastijan Vinko
F07 | Generiranje izvještaja | Korisnik će moći ispisati podatke aplikacije kao što su popis događaja, popis korisnika, popis moderatora, popis organizatora te popis događaja od organizatora. Prilikom pregledavanja izvještaja korisnik će moći spremiti izvještaj u obliku PDF-a.  | Sebastijan Vinko
F08 | Mogućnost izmjena tema aplikacije _(tamna/svijetla)_  i jezika _(hrvatski/engleski)_ | Mogućnost izmjene tema aplikacije, uključujući tamnu i svijetlu temu, omogućava korisnicima da prilagode izgled i boje aplikacije prema svojim preferencijama. Ova funkcionalnost omogućava promjenu estetskog izgleda aplikacije, a također može pružiti i praktične prednosti, kao što su smanjenje naprezanja očiju u tamnim uvjetima. Također omogućava korisnicima promjenu jezika sa Hrvatskog na Engleski jezik i obrnuto.	| Karlo Mikec
F09 | Upravljanje kategorijama | Administratori će moći dodavati nove kategorije događaja u listu postojećih kategorija događaja. Kod kreiranja događaja organizatori mogu poslati zahtjev za kreiranje nove kategorije sa nazivom i opisom te kategorije koje će onda administratori dobiti na pregled. Dobivene zahtjeve administratori mogu odbiti ili prihvatiti te mogu dobivenom zahtjevu promijeniti naziv. | Karlo Mikec
## Tehnologije i oprema
Aplikacija se oslanja na nekoliko ključnih tehnologija. Za modeliranje baze podataka, koristi se MySQL Workbench, što omogućuje precizno planiranje i organizaciju podataka. Za pohranu podataka, koristi se SQLite3, što je brza i pouzdana baza podataka koja osigurava sigurnu pohranu podataka. Kao backend servis za obradu podataka i komunikaciju s aplikacijom, koristi se Node.js koji je snažna JavaScript platforma za glatku izvedbu i brzu dostupnost podataka. Ove tehnologije omogućuju nam izradu stabilne i učinkovite baze podataka. Kao sustav za verzioniranje, koristi se Git i GitHub koji omogućuju učinkovito praćenje promjena u kodu. Za implementaciju same aplikacije kao razvojno okruženje koristi se Visual Studio, .NET Framework platforma za razvoj windows aplikacija te Windows Forms za kreiranje grafičkog korisničkog sučelja zajedno s C# programskim jezikom. Sva projektna dokumentacija dostupna je unutar GitHub Wiki. Za izradu dijagrama i vizualizaciju arhitekture aplikacije koristi se alat Visual Paradigm. Ova kombinacija tehnologija i alata osigurala je stabilan, transparentan i učinkovit razvoj aplikacije.
