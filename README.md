# protocol
<h3>Besprechung und Bearbeitung Github Aufgabe</h3>


<h2>Beginn Neues Projekt</h2>

[Github neues Projekt](https://github.com/neuefische/rem-21-3-github)

<h3>Module importieren: </h3>
File -> new File -> Module from Exisisting Sources -> Zielordner auswählen -> Next -> Finish

<h3>User stories:</h3>
 

 - Nicht-technische Beschreibung vom User erwünschte Funktionen
 - Technik ist dem User egal, allerdings Funktionalität und User Experience nicht

Neue Story (Github):
-> Issue-tab, dann neuer Eintrag
Methodik zur Bearbeitung:
-> Projects-Tab, dann dort je nach Entwicklungsstufe moven und fertigstellen

<h3>Swagger</h3>

 - Vorgefertigtes Frontend Framework
- wird über springfox-dependency eingeführt
- kann in der SwaggerConfig konfiguriert werden

Dependency:

    `<dependency>
    <groupId>io.springfox</groupId>
    <artifactId>springfox-boot-starter</artifactId>
    <version>3.0.0</version>
    </dependency>

Docket Starter:
````java
@Configuration
public class SpringFoxConfig {                                    
    @Bean
    public Docket api() { 
        return new Docket(DocumentationType.SWAGGER_2)  
          .select()                                  
          .apis(RequestHandlerSelectors.any())              
          .paths(PathSelectors.any())                          
          .build();                                           
    }
}
````
Test:
[http://localhost:8080/swagger-ui/](http://localhost:8080/swagger-ui/)

- In den RequestHandlerSelector eigenen backend einfügen statt any:
`.apis(RequestHandlerSelectors.basePackage("de.neuefische.name.backend"))`

<h3>Docker</h3>

 - Virtualisierung spezifisch für Anwendungen
- Containerbasiert
- hohe Effizienz aufgrund von minimalistischen Betriebssystemen
- Serialisierung von Containern

Installation testen:
`docker --version`
`docker-compose --version`
`docker stop <id>`
`docker stats` -> liefert ID der laufenden Container

<h3>PostgreSQL</h3>
Neue Database:
Docker starten
- Database -> Neue Database -> PostgreSQL -> generieren
