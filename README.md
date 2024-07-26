# Projet de Barre de Navigation Responsive

Ce projet consiste en la création d'une barre de navigation responsive. La barre de navigation s'adapte automatiquement à différentes tailles d'écran pour offrir une expérience utilisateur optimale sur tous les appareils.

## Fonctionnalités

- Affichage de la barre de navigation sur les écrans de bureau, tablettes et mobiles.
- Transition fluide entre les différentes tailles d'écran.
- Menu hamburger sur les petits écrans pour une navigation facile.
- Utilisation de CSS pour la gestion du responsive design.

## Technologies Utilisées

- HTML5
- CSS3
- JavaScript (si nécessaire pour le menu hamburger)

## Installation

Pour utiliser ce code sur votre propre projet, suivez ces étapes :

1. Clonez ce dépôt sur votre machine locale :
   ```bash
   git clone https://github.com/votre-utilisateur/navigation-responsive.git
   ```
2. Accédez au dossier du projet :
   ```bash
   cd navigation-responsive
   ```

## Utilisation

1.  **HTML**  
     Le fichier `index.html` contient la structure de la barre de navigation. Voici un exemple de la structure HTML :

        ```html

    <!DOCTYPE html>
    <html lang="en" dir="ltr">

<head>
    <meta charset="utf-8">
    <meta name="viewport" 
          content="width=device-width,
                   initial-scale=1.0">
    <link rel="stylesheet" href=
"https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <nav>
        <input type="checkbox" id="check">
        <label for="check" class="checkbtn">
            <i class="fas fa-bars"></i>
        </label>
        <label class="logo">Mike</label>
        <ul>
            <li><a class="active" href="#">HTML</a></li>
            <li><a href="#">JavaScript</a></li>
            <li><a href="#">ReactJS</a></li>
            <li><a href="#">NodeJS</a></li>
        </ul>
    </nav>
</body>

</html>
    ```

2. **CSS**  
   Le fichier `styles.css` contient le style pour la barre de navigation. Voici un exemple de code CSS pour rendre la barre de navigation responsive :

   ```css
/* style.css*/

body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
  }
  
  nav {
    background-color: green;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
  }
  
  .logo {
    font-size: 1.5rem;
  }
  
  ul {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  ul li {
    margin-right: 20px;
  }
  
  ul li a {
    color: white;
    text-decoration: none;
    transition: color 0.3s;
  }
  
  ul li a:hover {
    color: lightgreen;
  }
  
  .checkbtn {
    font-size: 30px;
    color: white;
    cursor: pointer;
    display: none;
  }
  
  #check {
    display: none;
  }
  
  @media (max-width: 768px) {
    .checkbtn {
      display: block;
      order: 1;
      margin-right: 20px;
    }
  
    ul {
      position: fixed;
      top: 80px;
      right: -100%;
      background-color: green;
      width: 100%;
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      transition: all 0.3s;
    }
  
    ul li {
      margin: 20px 0;
    }
  
    ul li a {
      font-size: 20px;
    }
  
    #check:checked ~ ul {
      right: 0;
    }
  }
   ```

3. **JavaScript**  
   Le fichier `script.js` contient le code JavaScript pour le menu hamburger. Voici un exemple de code JavaScript pour activer le menu :

   ```javascript
   const toggleButton = document.getElementsByClassName("toggle-button")[0];
   const navbarLinks = document.getElementsByClassName("navbar-links")[0];

   toggleButton.addEventListener("click", () => {
     navbarLinks.classList.toggle("active");
   });
   ```

## Contribuer

Les contributions sont les bienvenues ! Pour proposer des modifications, veuillez ouvrir une pull request.

## Auteurs

- **Mike Batelahoko** - Développeur principal

## Licence

Aucune licence