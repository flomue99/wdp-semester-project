# JSX  Jonas und Florian Muehleder

## Grobe Struktur der Presentation

### 1. Einleitung
- Thema der Presentation kurz vorstellen
- Was ist JSX?



JSX wurde 2011 von Facebook für die Verwendung von React entwickelt.
JSX ist eine Syntaxerweiterung für JavaScript, die es Entwicklern ermöglicht, HTML-ähnlichen Code innerhalb von JavaScript-Dateien zu schreiben
Es wird als sogenannter Syntax-Sugar bezeichnet.

### 2. Grundlagen von JSX
- Grundlagen der Syntax
- Vergleich zwischen JSX und JS anhand von Helloworld

**JSX**  
JSX vereinfach das erstellen von DOM-Elementen
```jsx
const element = <div>Hello, World!</div>;
```     

Verwendung von JS innherlab von html elementen  
```jsx
const name = 'John Doe';
const greeting = <p>Hallo, {name}!</p>;
```

**JS**  
In herkömmlichem JavaScript würden HTML-Elemente durch das Erstellen von DOM-Elementen und deren Manipulation erstellt werden
```js
const element = document.createElement('div');
element.textContent = 'Hello, World!';
document.body.appendChild(element);
```

## 3. Vorteile und Nachteile JSX

**VT:**  

-Lesbarkeit und Schreibweise
-Integration von JS in HTML
-Wiederverwendbarkeit von einzelnen Komponenten

**NT:**

- Mischung von HTML und Javascript, viele entwickler wollen JS und HTMl strikt trennen.
- Notwendigkeit eines Build-Tolls wie Babel um JSX im JS zu übersetzten


## 4. JSX -> JS
- wie sieht JSX als JS aus

## 5. Verwendung mit React
- Verwendung von Components
- Vorteile der verwendung

## 6. Beispiel mit React
- React Anwendung in der wir die Verwednung von JSX zeigen
- 3 Komponenten, (App, Table, Rows)
- Tabeller in der Zeilen hinzugefügt und entfernt werden könnnen

## 7. Zusammenfassung
- Zusammenfassung der Presentation


## Referenzliste

**Sehr WICHTIG!!**  
- https://kinsta.com/de/wissensdatenbank/was-ist-jsx/

- https://www.geeksforgeeks.org/what-are-the-advantages-of-using-jsx-in-reactjs/

- https://react.dev/

- https://legacy.reactjs.org/docs/jsx-in-depth.html

- https://www.udemy.com/course/the-ultimate-react-course/

- https://kinsta.com/knowledgebase/what-is-jsx/

- https://www.typescriptlang.org/docs/handbook/jsx.html

- https://transform.tools/html-to-jsx (html in jsx und umgekehrt)

- https://babeljs.io/ (javascipt compiler für jsx)



## code

### Wurzelelement
```jsx
//erlaubt
function Person() {
    return (
        <div>
            <span>Lastname</span>
            <span>Firstname</span>
        </div>
    );
}

//Nicht erlaubt, da es nur ein Wurzelelement geben darf
function MyButton() {
    return (
        <span>Lastname</span>
        <span>Firstname</span>
    );
}


//Verwendung von className anstelle von class
<div className="fancy-class">This element has a fancy CSS class.</div>

//sollte vermieden werden -> class ist ein reserviertes Schlüsselwort in JS
<div class="fancy-class">This element has a fancy CSS class.</div>



<div>{customer.firstname}</div>

<p>8 Byte = {8 * 8} bits</p>

<h1>{x > 50 ? "Positive" : "Negative"}</h1>

<div>
    {isAuthenticated ? (
        <button>Logout</button>
    ) : (
        <button>Login</button>
    )}
</div>



const grades = [
  { text: 'Very Good', number: 1 },
  { text: 'Good', number: 2 },
  { text: 'Satisfactory', number: 3 },
  { text: 'Adequate', number: 4 },
  { text: 'Unsatisfactory', number: 5 },
];

function AllGrades() {
  return (
    <ul>
      {grades.map(grade => (
        <li key={grade.number}>
          {grade.text} is {grade.number} as number.
        </li>
      ))}
    </ul>
  );
}

```