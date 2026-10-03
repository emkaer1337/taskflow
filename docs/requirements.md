# Funkcionális követelmények

### US-01 – Felhasználói jogosultságok kezelése

**Leírás:** Adminisztrátorként szeretném kezelni a rendszer többi felhasználójának jogosultságait, hogy az alapvető felhasználókezelési feladatokhoz ne legyen szükség fejlesztői beavatkozásra.

**Elfogadási kritériumok:**

* Az adminisztrátor az adminisztrációs felületen látja a rendszer felhasználóit és a hozzájuk rendelt jogosultságokat.
* A felhasználók szerepköre és jogosultságai módosíthatók, a változtatások pedig mentés után érvénybe lépnek.
* Normál felhasználók nem férhetnek hozzá az adminisztrációs felülethez.

### US-02 – SAML 2.0 alapú vállalati bejelentkezés (SSO)

**Leírás:** Felhasználóként szeretnék a vállalati fiókommal bejelentkezni az alkalmazásba, hogy ne kelljen külön felhasználói fiókot létrehoznom és újabb jelszót megjegyeznem.

**Elfogadási kritériumok:**

* A bejelentkezési oldalon elérhető a vállalati bejelentkezés lehetősége, amely a vállalati azonosítási felületre irányítja a felhasználót.
* Sikeres vállalati hitelesítés után a felhasználó hozzáfér az alkalmazáshoz.
* Sikertelen bejelentkezés esetén a felhasználó nem kap hozzáférést a rendszerhez, és erről visszajelzést kap.

# Nem funkcionális követelmények

### NFR-01 – Teljesítmény

**Leírás:** Az alkalmazásnak gördülékenyen kell működnie akkor is, ha egyszerre többen használják.

**Elfogadási kritériumok:**

* Az alkalmazás főoldala normál használat mellett legfeljebb 3 másodperc alatt betöltődik.
* A rendszer 50 egyidejű felhasználó esetén is megfelelő sebességgel működik, jelentős lassulás nélkül.

### NFR-02 – Biztonság

**Leírás:** A felhasználók adatai és a rendszerben tárolt információk nem kerülhetnek illetéktelen kezekbe.

**Elfogadási kritériumok:**

* A felhasználói jelszavak nem olvasható formában, biztonságos hash-eléssel kerülnek tárolásra az adatbázisban.
* A felhasználók kizárólag azokhoz a funkciókhoz és adatokhoz férhetnek hozzá, amelyekhez megfelelő jogosultsággal rendelkeznek.
