# Guía de XML

### Què és XML?
XML en anglès són les sigles de eXtensible Markup Language, el qual vol dir que és un llenguatge de marques amb el qual pots definir tu mateix les funcions i les marques. Està disenyat per a transportar i emmagatzemar dades entre aplicacions i desenvolupat de manera que sigui autodescriptiu.
El format en que s'emmagatzemen les dades està disenyat perquè es pugui llegir fàcilment i perquè la màquina ho pugui també desxifrar amb facilitat.
SMGL és la mare de XML i HTML i és d'on sorgeix aquest llenguatge de programació.
### Per a què serveix?
Com he esmentat anteriorment aquest llenguatge s'empra per a transportar, emmagatzemar i processar dades i és una forma de tenir-les accessible i còmode. També s'usa per a programes de desenvolupament de entorns interactius com android studio, que l'utilitza per a transportar les dades i donar format als diferents arxius que s'han de carregar en pantalla.

### Casos d'ús
Per exemple, en un banc, tindràn la seva base de dades, però normalment de la base de dades al lliurament d'aquestes dades hi ha un xml puix que en la base de dades la informació està molt optimitzada.

### Què és i per a què serveix el DTD?
El DTD o XSD (que és la versió més nova), és un "esquema" que té la funció de validar el codi XML prèviament escrit. Aquest document també el programem nosaltres i segons el que volguem validar haurem de prendre una sèrie de decisions.

Nosaltres podem crear les etiquetes que vulguem i perquè tot tingui sentit hem de crear un document XSD per validar la estructura del que hem creat. Per definir que tot allò que hem escrit té un sentit i una direcció funcional. Per això aquest esquema representa el que són els diferents formats:

* XML - Crea Etiquetes
* XSD - Valida les estructures
* DTD - Com XSD però més antic

### Programació XML:

Per començar a provar aquest llenguatge hem d'obrir el nostre editor de codi pereferit i començar un document XML.

#### Capçalera:
La capçalera en XML és la següent:
```XML
 <?xml version="1.0" encoding="UTF-8" ?>
```
Aquesta capçalera el que fa es definir la codificació de caràcters UTF-8, perquè si cambiem de país o regió no s'ens canvïn els caràcters.

#### Contingut: 
El contingut d'un document XML pot ésser molt variat però normalment s'hi escriuen variables:
Per definir una variable es fa de la següent manera:
```XML
<nom de la variable> variable </nom de la variable>
```
En canvi, si sabem sempre que la variable serà un tipus concret de dada es poden escriure variables d'aquesta manera més senzilla:
```XML
<nom_de_la_variable value="valor"/>
```
Un exemle de codi utilitzant el que acabo de mencionar podría ser aquest:
```XML
<?xml version="1.0" encoding="UTF-8" ?>
<character>
	<name>Eustaquio</name>
	<surname>Mendoza</surname>
	<!-- COMENTARIO -->
	<age value="197" />
</character>
```
##### DTD:
Per escriure el teu document DTD has de fer el següent:
La capçelera del document és la mateixa que a XML i el que haurem de fer és per cada variable de XML, hem de posar això:
```DTD
<!ELEMENT name #PCDATA>
<!ELEMENT surname #PCDATA>
<!ELEMENT age #PCDATA>
<!ATTLIST age value #REQUIRED>
```
D'auesta manera, on diu element son les variables i on diu attlist són els atributs de les variables, com en el cas de age: "value"







