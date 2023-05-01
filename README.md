
# Guía de XML

### Què és XML?
XML en anglès són les sigles de eXtensible Markup Language, el qual vol dir que és un llenguatge de marques amb el qual pots definir tu mateix les funcions i les marques. Està disenyat per a transportar i emmagatzemar dades entre aplicacions i desenvolupat de manera que sigui autodescriptiu.
El format en que s'emmagatzemen les dades està disenyat perquè es pugui llegir fàcilment i perquè la màquina ho pugui també desxifrar amb facilitat.
SMGL és la mare de XML i HTML i és d'on sorgeix aquest llenguatge de programació.

XML (Extended Markup Language) és el llenguatge base dels llenguatges de marques que tenim avui dia. XML no ve del no-res. Als anys 70 era SGML, s'utilitzava per marcar en documents el que era una negreta, una cursiva, ratllat etc. Ja que en aquella època no hi havia interfície gràfica. El driver de la impressora interpreta això, és a dir, el parsejava i posava les negretes, cursives… quan tocava. Arriben els 90, a banda d'inventar-se Linux, s'inventa Internet.

### Per a què serveix?
Com he esmentat anteriorment aquest llenguatge s'empra per a transportar, emmagatzemar i processar dades i és una forma de tenir-les accessible i còmode. També s'usa per a programes de desenvolupament de entorns interactius com android studio, que l'utilitza per a transportar les dades i donar format als diferents arxius que s'han de carregar en pantalla.

Hi han diferents tipus de formats:
* Text pla → fitxer que conté text sense format o estructura, és a dir, simplement una seqüència de caràcters. El text pla és llegible per als humans i es pot obrir i editar amb un editor de text simple.

* Text enriquit → És un text pla amb info extra. Es refereix a un fitxer que conté text amb formats addicionals com negretes, cursives, subratllats, mides de font, colors, etc. Per exemple, els meus apunts de Google Docs són text enriquit.

* Binari → Contenen dades en un format que no és llegible directament pels humans, sinó que està dissenyat per ser processat per ordinadors.

XML utilitza el text enriquit per a processar el seu codi.

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
Això és un exemple de variable **parella**.
En canvi, si sabem sempre que la variable serà un tipus concret de dada es poden escriure variables d'aquesta manera més senzilla:
```XML
<nom_de_la_variable value="valor"/>
```
Això és un exemple de variable **imparella**

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

Les diferents etiquetes són:

#REQUIRED: Aquesta etiqueta s'utilitza per especificar que un atribut és obligatori per a un element determinat. Si un atribut amb aquesta etiqueta no s'especifica al document XML, es produeix un error de validació.

#PCDATA: Aquesta etiqueta s'utilitza per especificar que un element només pot contenir dades de text pla (text sense format), sense etiquetes XML ni caràcters especials. És a dir, l'element no pot contenir subelements, només text.

#EMPTY: Aquesta etiqueta es fa servir per especificar que un element no pot contenir contingut. És a dir, un element amb aquesta etiqueta no pot tenir text o subelements. S'utilitza per a elements que actuen com a contenidors buits, com ara les etiquetes de salt de línia, les etiquetes de tancament, etc.