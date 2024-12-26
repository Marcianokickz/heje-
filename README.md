<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sérénité Citoyenne</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        header {
            background: #2a9d8f;
            color: #fff;
            padding: 1rem 0;
        }

        header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        header nav ul {
            list-style: none;
            display: flex;
        }

        header nav ul li {
            margin: 0 1rem;
        }

        header nav ul li a {
            color: #fff;
            text-decoration: none;
        }

        .hero {
            background: #264653;
            color: #fff;
            text-align: center;
            padding: 2rem 1rem;
        }

        .hero .cta {
            background: #e9c46a;
            color: #000;
            padding: 0.5rem 1rem;
            text-decoration: none;
            margin-top: 1rem;
            display: inline-block;
        }

        .services {
            padding: 2rem 1rem;
            text-align: center;
        }

        .service-item {
            background: #f4a261;
            margin: 1rem 0;
            padding: 1rem;
            border-radius: 5px;
        }

        .contact {
            padding: 2rem 1rem;
            background: #e76f51;
            color: #fff;
        }

        footer {
            text-align: center;
            padding: 1rem;
            background: #264653;
            color: #fff;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Sérénité Citoyenne</h1>
            <nav>
                <ul>
                    <li><a href="#accueil">Accueil</a></li>
                    <li><a href="#services">Nos Services</a></li>
                    <li><a href="#simulateur">Simulateur</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="accueil" class="hero">
            <h2>Facilitez vos démarches de naturalisation</h2>
            <p>Votre partenaire de confiance pour les titres de séjour et la citoyenneté française.</p>
            <a href="#simulateur" class="cta">Simulez votre éligibilité</a>
        </section>

        <section id="services" class="services">
            <h2>Nos Services</h2>
            <div class="service-item">
                <h3>Naturalisation</h3>
                <p>Accompagnement complet pour devenir citoyen français.</p>
            </div>
            <div class="service-item">
                <h3>Régularisation</h3>
                <p>Aide pour résoudre les situations administratives complexes.</p>
            </div>
            <div class="service-item">
                <h3>Conseil juridique</h3>
                <p>Consultation avec nos avocats spécialisés.</p>
            </div>
        </section>

        <section id="simulateur" class="simulateur">
            <h2>Simulateur d'éligibilité</h2>
            <form id="eligibility-form">
                <label for="age">Âge :</label>
                <input type="number" id="age" name="age" required>

                <label for="status">Statut actuel :</label>
                <select id="status" name="status" required>
                    <option value="etudiant">Étudiant</option>
                    <option value="travailleur">Travailleur</option>
                    <option value="autre">Autre</option>
                </select>

                <button type="submit">Simuler</button>
            </form>
            <p id="result"></p>
        </section>

        <section id="contact" class="contact">
            <h2>Contactez-nous</h2>
            <form>
                <label for="name">Nom :</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email :</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message :</label>
                <textarea id="message" name="message" required></textarea>

                <button type="submit">Envoyer</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Sérénité Citoyenne. Tous droits réservés.</p>
    </footer>

    <script>
        document.getElementById('eligibility-form').addEventListener('submit', function (e) {
            e.preventDefault();
            const age = document.getElementById('age').value;
            const status = document.getElementById('status').value;

            let result = '';
            if (age >= 18 && status !== 'autre') {
                result = 'Vous êtes probablement éligible. Contactez-nous pour une évaluation complète.';
            } else {
                result = 'Vous ne semblez pas éligible pour le moment.';
            }

            document.getElementById('result').textContent = result;
        });
    </script>
</body>
</html>



