# README
**DHCP (Dynamic Host Configuration Protocol)** i **Gateway** su dva ključna pojma u računarstvu i mrežama, a evo šta oni znače:

### 1. **DHCP (Dynamic Host Configuration Protocol)**:

DHCP je protokol koji automatski dodeljuje IP adrese uređajima u mreži. Umesto da korisnik ručno postavlja IP adresu za svaki uređaj, DHCP server to radi automatski. Kada se uređaj poveže na mrežu, DHCP server mu dodeljuje IP adresu, kao i druge potrebne informacije (kao što su DNS serveri i default gateway) kako bi uređaj mogao da komunicira sa drugim uređajima na mreži ili internetu.

**Kako funkcioniše DHCP**:

- Uređaj (npr. računar, telefon) koji se povezuje na mrežu šalje zahtev DHCP serveru.
- DHCP server odgovara dodeljivanjem slobodne IP adrese iz svog opsega (pool-a).
- Ovaj proces omogućava jednostavno povezivanje uređaja u mreži bez potrebe za manuelnim postavljanjem IP adresa.

### 2. **Gateway**:

Gateway (ili "ulazna tačka") je uređaj koji povezuje dve mreže i omogućava komunikaciju između njih. Najčešće se koristi kao uređaj koji povezuje lokalnu mrežu (LAN) sa širim mrežama kao što je internet (WAN). Gateway preusmerava saobraćaj između različitih mrežnih segmenata, i obično je prvi uređaj na koji se upućuje mrežni saobraćaj kada uređaj u lokalnoj mreži želi da komunicira sa spoljnim svetom (npr. internetom).

**Kako funkcioniše Gateway**:

- Uređaj u lokalnoj mreži šalje podatke ka gateway-u kada želi da pristupi internetu ili drugim spoljnim resursima.
- Gateway zatim prosleđuje podatke ka odredišnoj mreži (npr. internetu) i vrati odgovor korisniku.

**Kombinacija u mrežama**:

- DHCP server dodeljuje IP adresu uređaju, a kao deo tih informacija, uređaj često dobija i IP adresu gateway-a. Ovo omogućava uređaju da zna preko kojeg uređaja treba da prosledi saobraćaj prema spoljnim mrežama, kao što je internet.

Ukratko:

- **DHCP** automatski dodeljuje IP adrese uređajima na mreži.
- **Gateway** je uređaj koji omogućava komunikaciju između različitih mreža, najčešće između lokalne mreže i interneta.

### 1. **Portovi (Ports)**

U računarskim mrežama, **portovi** su virtualni "ulazi" koji omogućavaju različitim aplikacijama na računaru ili uređaju da komuniciraju putem mreže. Svaka aplikacija ili usluga na računaru koristi specifičan port da bi primala ili slala podatke. Portovi su numerisani brojevima od 0 do 65535, i oni se dele u tri kategorije:

- **Well-known ports (poznati portovi)**: Brojevi portova od 0 do 1023. Ovi portovi su rezervisani za najpoznatije i najkoristjenije usluge. Na primer:
    
    - **Port 80**: HTTP (web saobraćaj)
    - **Port 443**: HTTPS (siguran web saobraćaj)
    - **Port 21**: FTP (File Transfer Protocol)
- **Registered ports (registrovani portovi)**: Brojevi portova od 1024 do 49151. Ovi portovi se koriste za aplikacije koje nisu univerzalno prepoznate, ali su registrovane za specifične usluge.
    
- **Dynamic/Private ports (dinamički/privatni portovi)**: Brojevi portova od 49152 do 65535. Ovi portovi se obično koriste za privremene veze, često kao portovi za klijent-server komunikaciju.
    

### 2. **Protokoli (Protocols)**

**Protokoli** su skup pravila koja određuju kako računari komuniciraju preko mreže. Postoje mnogi protokoli, a neki od najpoznatijih su:

- **TCP (Transmission Control Protocol)**: Pouzdan protokol koji obezbeđuje da podaci stignu u ispravnom redosledu. TCP koristi uspostavu veze (3-way handshake) i kontroliše greške.
    
- **UDP (User Datagram Protocol)**: Manje pouzdan protokol od TCP-a. Ne garantuje ispravnost podataka niti redosled. Koristi se kada je brzina važnija od pouzdanosti, kao što je kod strimovanja videa ili online igrica.
    
- **IP (Internet Protocol)**: Koristi se za adresiranje i usmeravanje podataka između uređaja na mreži. IP adresa identifikuje uređaj na mreži.
    
- **HTTP (Hypertext Transfer Protocol)**: Koristi se za prenos web stranica preko interneta.
    
- **HTTPS (Hypertext Transfer Protocol Secure)**: Sigurna verzija HTTP-a koja koristi enkripciju za zaštitu podataka.
    

### 3. **Maska podmreže (Subnet Mask)**

**Maska podmreže** je način za podelu IP adrese na dve komponente: deo koji identifikuje mrežu i deo koji identifikuje uređaj unutar te mreže. Maska se koristi da bi se odredilo koje IP adrese pripadaju istoj mreži.

Na primer, IP adresa može izgledati ovako: **192.168.1.100**, a maska podmreže može biti **255.255.255.0**. U ovom primeru:

- Maska **255.255.255.0** znači da prva tri okteta (192.168.1) identifikuju mrežu, dok četvrti oktet (100) identifikuje uređaj unutar te mreže.

Postoje i **CIDR** (Classless Inter-Domain Routing) notacije koje koriste `/` znak i broj, kao što je **192.168.1.100/24**, što znači da se prva 24 bita koriste za identifikaciju mreže.

### 4. **Primeri povezivanja portova, protokola i maski**

- **Port 80 (HTTP)** koristi **TCP** kao protokol za slanje web saobraćaja.
- **Port 443 (HTTPS)** koristi **TCP** i omogućava siguran web saobraćaj.
- **Maska podmreže** kao što je **255.255.255.0** pomaže uređajima unutar mreže da identifikuju koje IP adrese su deo njihove lokalne mreže.

Da li ste želeli detalje o nečemu specifičnom u vezi sa portovima, protokolima ili mrežnim maskama?


**DNS rekordi** (Domain Name System records) su informacije koje se čuvaju u DNS sistemu i omogućavaju pravilno usmeravanje internetskog saobraćaja na odgovarajuće servere. DNS je "telefon knjiga" interneta, jer prevodi ljudski čitljive domene, poput **[www.example.com](http://www.example.com)**, u IP adrese koje računari koriste za komunikaciju. DNS rekordi omogućavaju različite funkcije, kao što su prepoznavanje servera, usmeravanje e-pošte, ili prepoznavanje drugih usluga.

Evo osnovnih tipova DNS rekorda:

### 1. **A (Address) rekord**

- **A rekord** mapira domen na **IPv4 adresu**.
    
- Ovaj rekord se koristi da poveže naziv domena (npr. **example.com**) sa odgovarajućom IP adresom (npr. **192.168.1.1**).
    
    **Primer:**  
    `example.com. A 192.168.1.1`
    

### 2. **AAAA rekord**

- **AAAA rekord** mapira domen na **IPv6 adresu**.
    
- Slično kao A rekord, ali koristi IPv6 adresu (npr. **2001:0db8:85a3:0000:0000:8a2e:0370:7334**).
    
    **Primer:**  
    `example.com. AAAA 2001:0db8:85a3::8a2e:0370:7334`
    

### 3. **MX (Mail Exchange) rekord**

- **MX rekord** se koristi za određivanje **servera za e-poštu** koji je odgovoran za prijem e-mail poruka za određeni domen.
    
- Ovaj rekord sadrži prioritet (manji broj znači viši prioritet) i adresu servera za e-poštu.
    
    **Primer:**  
    `example.com. MX 10 mail.example.com.`  
    Ovdje broj 10 označava prioritet, a **mail.example.com** je mail server koji prima e-poštu za **example.com**.
    

### 4. **CNAME (Canonical Name) rekord**

- **CNAME rekord** omogućava da se **jedan domen aliasira** na drugi domen. To znači da možete imati više domena koji ukazuju na isti server.
    
- Na primer, možete napraviti alias za www, tako da **[www.example.com](http://www.example.com)** pokazuje na **example.com**.
    
    **Primer:**  
    `www.example.com. CNAME example.com.`
    

### 5. **NS (Name Server) rekord**

- **NS rekord** označava koji **DNS server** je odgovoran za upravljanje određenim domenom. Ovaj rekord se koristi za delegiranje kontrole nad domenom.
    
    **Primer:**  
    `example.com. NS ns1.nameserver.com.`  
    Ovdje **ns1.nameserver.com** je DNS server koji upravlja domenom **example.com**.
    

### 6. **PTR (Pointer) rekord**

- **PTR rekord** je suprotan od **A** i **AAAA** rekorda. Koristi se za obavljanje **reverse DNS lookup** – tj. za prepoznavanje domena na osnovu IP adrese.
    
- Ovaj rekord omogućava da pronađete naziv domena koji je povezan s određenom IP adresom.
    
    **Primer:**  
    `1.0.168.192.in-addr.arpa. PTR example.com.`  
    Ovdje se IP adresa **192.168.0.1** mapira na naziv domena **example.com**.
    

### 7. **SOA (Start of Authority) rekord**

- **SOA rekord** označava početak autoritativnih informacija o DNS zoni. Ovaj rekord sadrži informacije o DNS serverima koji su odgovorni za domenu, kao i parametre poput broja verzije zone i vremena osvežavanja.
    
    **Primer:**  
    `example.com. SOA ns1.nameserver.com. hostmaster.example.com. (2024010101 3600 1800 1209600 86400)`  
    Ovdje je **ns1.nameserver.com** autoritativni DNS server, **hostmaster.example.com** je kontakt adresa, a brojevi označavaju različite parametre za osvežavanje i vreme zadržavanja.
    

### 8. **TXT (Text) rekord**

- **TXT rekord** je fleksibilan DNS rekord koji se koristi za čuvanje različitih tekstualnih informacija o domenima, kao što su verifikacija vlasništva domena ili postavke sigurnosti.
    
- Na primer, **SPF (Sender Policy Framework)** koristi TXT rekorde za verifikaciju dozvoljenih servera za slanje e-pošte sa određenog domena.
    
    **Primer:**  
    `example.com. TXT "v=spf1 include:_spf.google.com ~all"`
    

### 9. **SRV (Service) rekord**

- **SRV rekord** koristi se za označavanje specifičnih servisa unutar domene, kao što su VoIP usluge ili chat servisi.
    
- SRV rekord uključuje protokol, servis, prioritet, težinu, port i odredišnu adresu.
    
    **Primer:**  
    `_sip._tcp.example.com. SRV 10 60 5060 sipserver.example.com.`  
    Ovdje je usluga **SIP (Session Initiation Protocol)** postavljena za protokol **TCP** na portu **5060**.
    

### 10. **CAA (Certification Authority Authorization) rekord**

- **CAA rekord** omogućava vlasnicima domena da kontrolišu koje **sertifikacione vlasti (CAs)** mogu izdatiti SSL/TLS sertifikate za njihov domen. Time se dodaje dodatni sloj zaštite od neautorizovanih sertifikata.
    
    **Primer:**  
    `example.com. CAA 0 issue "letsencrypt.org"`
    

### Zaključak

DNS rekordi omogućavaju raznovrsne funkcije u mrežama i na internetu, od mapiranja domena na IP adrese, do postavki za e-poštu i usluge kao što je HTTPS. Razumevanje različitih tipova DNS rekorda je ključno za pravilno upravljanje domenima, sigurnost i konfiguraciju mreže. Da li želite dodatne informacije o konfiguraciji nekih od ovih rekorda?
