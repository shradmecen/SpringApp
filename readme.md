Podsumowanie:
- Projekt jest podstawową aplikacja Spring Boot, która demonstruje prostą aplikację internetową z kontrolerem oraz szablonem HTML opartym na Thymeleaf. Została zaprojektowana jako wprowadzenie do tworzenia dynamicznych stron internetowych przy użyciu Spring Boot i Thymeleaf.

Funkcjonalności:
 1. Strona wyświetla wiadomość powitalną przy użyciu głównego adresu URL http://localhost:8080/
 2. Strona z dynamicznym powitaniem: Umożliwia personalizowane powitanie przy użyciu parametrów zapytania (/greeting?name=TwojeImię).

Opis działania:
1. Aplikacja rozpoczyna działanie od klasy VistulaApplication, która za pomocą SpringApplication.run() uruchamia aplikację Spring Boot.
2. Klasa HelloController definiuje dwa endpointy:
    - Główny endpoint (/): Wyświetla statyczną wiadomość powitalną.
    - Endpoint powitania (/greeting): Akceptuje parametr zapytania "name" i wyświetla spersonalizowane powitanie. Jeśli parametr name nie zostanie podany, domyślnie używane jest "World".
3. Plik greeting.html to szablon Thymeleaf, który dynamicznie renderuje wiadomość powitalną.

Case study:
- Scenariusz 1: Odwiedzanie strony głównej
    - URL: http://localhost:8080/
    - Przeglądarka wyświetla tekst: Hello Vistula, in my first Spring controller.

- Scenariusz 2: Powitanie użytkownika
    - URL: http://localhost:8080/greeting?name=Geralt
    - HelloController pobiera parametr name ("Geralt") i przekazuje go do szablonu greeting.html.
    - Renderowana strona HTML wyświetla: 
      Hello, Geralt!
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
    - Wyświetlane jest również logo z katalogu images.

- Scenariusz 3: Domyślne powitanie
    - URL: http://localhost:8080/greeting
    - Parametr "name" nie został podany.
    - Używana jest wartość domyślna "World", a renderowana strona wyświetla: Hello, World!
