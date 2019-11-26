<html style="background-color:lavender;">

<head>
    <meta charset="utf-8">
</head>

<body prefix="schema: http://schema.org">
    <header>
        <h1>
            E-card Web Editor raport
        </h1>
        <div role="contentinfo">
            <section typeof="sa:AuthorsList">
                <h3>Autori</h3>
                <ul>
                    <li typeof="sa:ContributorRole" property="schema:author">
                        <span typeof="schema:Person">
                            <meta property="schema:givenName" content="Marius">
                            <meta property="schema:additionalName" content="Marian">
                            <meta property="schema:familyName" content="Blaj">
                            <span property="schema:name">Marius M. Blaj</span>
                        </span>
                        <ul>
                            <li property="schema:roleContactPoint" typeof="schema:ContactPoint">
                                <a href="mailto:marius.blaj@info.uaic.ro" property="schema:email">marius.blaj@info.uaic.ro</a>
                            </li>
                        </ul>
                    </li>
                </ul>
                <ul>
                    <li typeof="sa:ContributorRole" property="schema:author">
                        <span typeof="schema:Person">
                            <meta property="schema:givenName" content="Lavinia">
                            <meta property="schema:familyName" content="Disca">
                            <span property="schema:name">Lavinia Disca</span>
                        </span>
                        <ul>
                            <li property="schema:roleContactPoint" typeof="schema:ContactPoint">
                                <a href="mailto:lavinia.disca@info.uaic.ro" property="schema:email">lavinia.disca@info.uaic.ro</a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </section>
        </div>
    </header>
    <section typeof="sa:Abstract" id="abstract" role="doc-abstract">
        <h3>Introducere</h3>
        <p>
            E-card Web Editor(ECaW) este o aplicatie web extensibila pentru crearea digitala a unor ilustrate de diverse categorii si impartasirea acestora cu cei dragi. Utilizatorii vor avea la dispozitie un canvas unde vor putea crea cardul dorit.
        </p>
    </section>
    <section id="techs">
        <h3>Tehnologii utilizate</h3>
        <ul>
            <li>JavaScript pentru implementarea functionalitatilor</li>
            <li>HTML si CSS pentru vizualizarea paginilor,respectiv pentru stilizarea lor</li>
            <li>MongoDB pentru managementul bazei de date</li>
            <li>Node.js pentru implementarea serverului</li>
        </ul>
    </section>
    <section id="pages">
        <h3>Paginile Web</h3>
        <ul>
            <li>
                <b>Login</b>: Utilizatorii se vor putea loga fie cu contul de facebook, fie cu contul de ECaW. Login-ul este necesar pentru a avea acces la proiectele personale sau la cele private la care are acces oferit de owner-ul proiectului.
            </li>
            <li>
                <b>Register</b>: In cazul in care utilizatorul nu are cont pe platforma, acesta isi va putea crea unul pe aceasta pagina.
            </li>
            <li>
                <b>Home</b>: Aici utilizatorul va putea vedea lista proiectelor la care are acces, sau sa creeze un nou proiect. Va putea vedea continutul fiecarui proiect pentru a-l edita, descarca sau a-l impartasi pe Facebook, email, etc.
            </li>
            <li>
                <b>Edit</b>: Pe aceasta pagina utilizatorul isi va putea da frau liber imaginatiei. Aici va putea sa isi creeze cardul pe care il doreste si sa impartaseasca accesul la proiect cu alti utilzatori.
            </li>
        </ul>
    </section>
    <section id="tools">
        <h3>Instrumente disponibile</h3>
        <ul>
            <li>
                <b>Pencil drawing</b>: Deseneaza linii pe canvas.
            </li>
            <li>
                <b>Text</b>: Inseareaza text.
            </li>
            <li>
                <b>Shape</b>: Creeaza o forma simpla(patrat, dreptunghi, stea, etc).
            </li>
            <li>
                <b>Photo</b>: Inseareaza poze de pe dispozitivul local sau de pe API-ul de la Imgur.
            </li>
            <li>
                <b>Resize</b>: Ajusteaza marimea oricarui obiect desenat.
            </li>
            <li>
                <b>Insert audio</b>: Adauga fundal sonor la proiect printr-un fisier .mp3 local.
            </li>
            <li>
                <b>Save</b>: Salveaza proiectul in baza de date.
            </li>
            <li>
                <b>Share</b>: Impartaseste proiectul fie pe retele sociale, email, etc./ Permite accesul altor utilizatori sa isi adauge contributia la proiect.
            </li>

        </ul>
    </section>
    <section id="server">
        <h3>
            Server end points
        </h3>
        <ul>
            <li>
                <b>/login</b>: Va verifica credentialele utilizatorului.
            </li>
            <li>
                <b>/register</b>: Va crea contul utilizatorului.
            </li>
            <li>
                <b>/projects</b>: Va trimite proiectele utilizatorului.
            </li>
            <li>
                <b>/projects/{id}</b>: In functie de tipul cererii(GET/POST/DELETE) va trimite proiectul cu acel id, va suprascrie proiectul respectiv va sterge proiectul.
            </li>
        </ul>
    </section>
    <section>
        <h3>
            API-uri folosite
        </h3>
        <ul>
            <li>
                <b>Imgur</b>: Va furniza pozele pe care le vor cauta utilizatorii in interiorul aplicatiei, pentru a fi incluse in proiect.
            </li>
        </ul>
    </section>
    <section>
        <h3>Arhitectura aplicatiei: MVC</h3>
        <figure typeof="sa:image">
            <img src="MVC.png" alt="MVC Diagram">
        </figure>
        <p>
            <ul>
                <li><b>View</b>: reprezinta interfata grafica cu care interactioneaza utilizatorul</li>
                <li><b>Controller</b>: interpreteaza inputurile provenite din View</li>
                <li><b>Model</b>: trimite cereri serverului si proceseaza raspunsurile primite</li>
                <li><b>Server</b>: se ocupa de managementul bazei de date si de autentificarea utilizatorilor</li>
            </ul>
        </p>
    </section>
    <section>
        <h3>Database Diagram</h3>
        <figure typeof="sa:image">
            <img src="dbdiagram.png" alt="Database Diagram">
        </figure>
    </section>
</body>

</html>