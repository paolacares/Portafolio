# Portafolio
Portafolio web de diseño gráfico de Paola Cares
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>PULGA SAD® — Graphic Designer</title>

    <meta
        name="description"
        content="Portfolio de Paola Cares — Graphic Designer especializada en branding, publicidad y diseño digital."
    >

    <style>

        /* ========================================
           RESET
        ======================================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #111111;
            color: #f1f0ea;
            line-height: 1.4;
        }

        a {
            color: inherit;
            text-decoration: none;
        }


        /* ========================================
           VARIABLES
        ======================================== */

        :root {
            --black: #111111;
            --cream: #f1f0ea;
            --gray: #8c8c87;
            --lime: #d9ff00;
            --border: rgba(241, 240, 234, 0.18);
        }


        /* ========================================
           HEADER
        ======================================== */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;

            display: flex;
            justify-content: space-between;
            align-items: center;

            padding: 24px 5vw;

            background: rgba(17, 17, 17, 0.82);
            backdrop-filter: blur(12px);

            border-bottom: 1px solid var(--border);
        }

        .logo {
            font-size: 18px;
            font-weight: 800;
            letter-spacing: -0.04em;
        }

        .logo span {
            color: var(--lime);
        }

        nav {
            display: flex;
            gap: 32px;
        }

        nav a {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 0.12em;
            color: var(--gray);

            transition: 0.3s ease;
        }

        nav a:hover {
            color: var(--cream);
        }


        /* ========================================
           HERO
        ======================================== */

        .hero {
            min-height: 100vh;

            display: flex;
            flex-direction: column;
            justify-content: center;

            padding: 140px 5vw 80px;

            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: "";
            position: absolute;

            width: 500px;
            height: 500px;

            right: -180px;
            top: 20%;

            border-radius: 50%;

            background: var(--lime);

            filter: blur(120px);
            opacity: 0.07;
        }

        .hero-small {
            color: var(--lime);
            font-size: 12px;
            letter-spacing: 0.18em;
            text-transform: uppercase;

            margin-bottom: 25px;
        }

        .hero h1 {
            font-size: clamp(70px, 13vw, 190px);
            line-height: 0.78;
            letter-spacing: -0.08em;
            font-weight: 800;
        }

        .hero h1 span {
            display: block;
            color: transparent;

            -webkit-text-stroke: 1px var(--cream);
        }

        .hero-description {
            max-width: 520px;

            margin-top: 50px;

            color: var(--gray);
            font-size: 17px;
        }

        .hero-description strong {
            color: var(--cream);
        }

        .scroll {
            position: absolute;
            bottom: 35px;
            left: 5vw;

            color: var(--gray);

            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 0.15em;
        }


        /* ========================================
           GENERAL SECTIONS
        ======================================== */

        section {
            padding: 120px 5vw;
        }

        .section-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-end;

            margin-bottom: 60px;

            border-bottom: 1px solid var(--border);
            padding-bottom: 20px;
        }

        .section-number {
            color: var(--lime);
            font-size: 11px;
        }

        .section-title {
            font-size: 12px;
            text-transform: uppercase;
            letter-spacing: 0.15em;
        }


        /* ========================================
           PROJECT GRID
        ======================================== */

        .projects {
            display: grid;

            grid-template-columns: repeat(2, 1fr);

            gap: 70px 30px;
        }

        .project {
            cursor: pointer;
        }

        .project-image {
            aspect-ratio: 4 / 3;

            background:
                linear-gradient(
                    135deg,
                    #252525,
                    #171717
                );

            overflow: hidden;

            position: relative;

            transition: transform 0.5s ease;
        }

        .project:nth-child(2) .project-image {
            background:
                linear-gradient(
                    135deg,
                    #303030,
                    #111111
                );
        }

        .project:nth-child(3) .project-image {
            background:
                linear-gradient(
                    135deg,
                    #191919,
                    #343434
                );
        }

        .project:nth-child(4) .project-image {
            background:
                linear-gradient(
                    135deg,
                    #292929,
                    #151515
                );
        }

        .project:nth-child(5) .project-image {
            background:
                linear-gradient(
                    135deg,
                    #171717,
                    #2c2c2c
                );
        }

        .project:nth-child(6) .project-image {
            background:
                linear-gradient(
                    135deg,
                    #333333,
                    #151515
                );
        }

        .project-image::after {
            content: "VIEW PROJECT";

            position: absolute;

            left: 50%;
            top: 50%;

            transform: translate(-50%, -50%) scale(0.8);

            opacity: 0;

            padding: 14px 20px;

            background: var(--lime);
            color: var(--black);

            font-size: 10px;
            font-weight: bold;
            letter-spacing: 0.1em;

            transition: 0.4s ease;
        }

        .project:hover .project-image {
            transform: scale(0.98);
        }

        .project:hover .project-image::after {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1);
        }

        .project-info {
            display: flex;
            justify-content: space-between;

            padding-top: 16px;

            border-top: 1px solid var(--border);

            margin-top: 12px;
        }

        .project-name {
            font-size: 16px;
        }

        .project-category {
            color: var(--gray);
            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 0.08em;
        }


        /* ========================================
           ABOUT
        ======================================== */

        .about {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 80px;
        }

        .about h2 {
            font-size: clamp(45px, 6vw, 85px);
            line-height: 0.95;
            letter-spacing: -0.06em;
        }

        .about h2 span {
            color: var(--lime);
        }

        .about-text {
            color: var(--gray);
            font-size: 17px;
            max-width: 500px;
        }

        .about-text p {
            margin-bottom: 30px;
        }


        /* ========================================
           SKILLS
        ======================================== */

        .skills {
            margin-top: 50px;

            display: flex;
            flex-wrap: wrap;

            gap: 10px;
        }

        .skill {
            border: 1px solid var(--border);

            padding: 10px 15px;

            font-size: 11px;
            text-transform: uppercase;
            letter-spacing: 0.08em;
        }


        /* ========================================
           CONTACT
        ======================================== */

        .contact {
            min-height: 70vh;

            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .contact h2 {
            font-size: clamp(55px, 10vw, 140px);
            line-height: 0.85;
            letter-spacing: -0.07em;
        }

        .contact h2 span {
            color: var(--lime);
        }

        .contact-email {
            margin-top: 50px;

            font-size: clamp(20px, 3vw, 35px);

            border-bottom: 1px solid var(--cream);

            width: fit-content;

            transition: 0.3s ease;
        }

        .contact-email:hover {
            color: var(--lime);
            border-color: var(--lime);
        }

        .socials {
            display: flex;
            gap: 25px;

            margin-top: 30px;
        }

        .socials a {
            font-size: 11px;

            text-transform: uppercase;
            letter-spacing: 0.1em;

            color: var(--gray);

            transition: 0.3s ease;
        }

        .socials a:hover {
            color: var(--lime);
        }


        /* ========================================
           FOOTER
        ======================================== */

        footer {
            padding: 30px 5vw;

            display: flex;
            justify-content: space-between;

            border-top: 1px solid var(--border);

            color: var(--gray);

            font-size: 10px;
            text-transform: uppercase;
            letter-spacing: 0.1em;
        }


        /* ========================================
           MODAL
        ======================================== */

        .modal {
            position: fixed;

            inset: 0;

            background: rgba(0, 0, 0, 0.9);

            z-index: 2000;

            display: none;

            align-items: center;
            justify-content: center;

            padding: 30px;
        }

        .modal.active {
            display: flex;
        }

        .modal-content {
            max-width: 800px;
            width: 100%;

            background: #181818;

            padding: 40px;

            position: relative;

            border: 1px solid var(--border);
        }

        .modal-close {
            position: absolute;

            right: 20px;
            top: 20px;

            background: none;
            border: none;

            color: var(--cream);

            font-size: 25px;

            cursor: pointer;
        }

        .modal h2 {
            font-size: 45px;
            line-height: 1;
            margin-bottom: 20px;
        }

        .modal p {
            color: var(--gray);
            margin-bottom: 30px;
        }

        .behance-button {
            display: inline-block;

            background: var(--lime);
            color: var(--black);

            padding: 14px 20px;

            font-size: 11px;
            font-weight: bold;

            text-transform: uppercase;
            letter-spacing: 0.1em;
        }


        /* ========================================
           RESPONSIVE
        ======================================== */

        @media (max-width: 768px) {

            header {
                padding: 20px;
            }

            nav {
                gap: 15px;
            }

            nav a {
                font-size: 10px;
            }

            .hero {
                padding-left: 20px;
                padding-right: 20px;
            }

            section {
                padding: 80px 20px;
            }

            .projects {
                grid-template-columns: 1fr;
                gap: 50px;
            }

            .about {
                grid-template-columns: 1fr;
                gap: 40px;
            }

            .project-info {
                flex-direction: column;
                gap: 8px;
            }

            footer {
                padding: 25px 20px;
                flex-direction: column;
                gap: 10px;
            }

        }

    </style>
</head>


<body>


<!-- ========================================
     HEADER
======================================== -->

<header>

    <a href="#" class="logo">
        PULGA <span>SAD®</span>
    </a>

    <nav>
        <a href="#work">Work</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </nav>

</header>


<!-- ========================================
     HERO
======================================== -->

<main>

<section class="hero">

    <div class="hero-small">
        Graphic Designer · Concepción, Chile
    </div>

    <h1>
        PAOLA
        <span>CARES</span>
    </h1>

    <p class="hero-description">
        Diseñadora gráfica enfocada en
        <strong>branding, publicidad y diseño digital.</strong>
        Creo piezas visuales que combinan concepto,
        comunicación y personalidad.
    </p>

    <div class="scroll">
        ↓ Scroll to explore
    </div>

</section>


<!-- ========================================
     WORK
======================================== -->

<section id="work">

    <div class="section-header">

        <div class="section-number">
            01 / 06
        </div>

        <div class="section-title">
            Selected Work
        </div>

    </div>


    <div class="projects">


        <!-- PROJECT 01 -->

        <article
            class="project"
            onclick="openProject(
                'Gráficas Proyecto',
                'Diseño gráfico · Publicidad',
                'https://www.behance.net/gallery/253653869/PORTFOLIO'
            )"
        >

            <div class="project-image"></div>

            <div class="project-info">

                <div class="project-name">
                    Gráficas Proyecto
                </div>

                <div class="project-category">
                    Advertising
                </div>

            </div>

        </article>


        <!-- PROJECT 02 -->

        <article
            class="project"
            onclick="openProject(
                'Invitación y Cuadro Libro de Firmas',
                'Diseño editorial · Matrimonio',
                'https://www.behance.net/gallery/253653869/PORTFOLIO'
            )"
        >

            <div class="project-image"></div>

            <div class="project-info">

                <div class="project-name">
                    Invitación & Libro de Firmas
                </div>

                <div class="project-category">
                    Editorial
                </div>

            </div>

        </article>


        <!-- PROJECT 03 -->

        <article
            class="project"
            onclick="openProject(
                'Diseño folleto matrimonio',
                'Diseño editorial',
                'https://www.behance.net/gallery/253653869/PORTFOLIO'
            )"
        >

            <div class="project-image"></div>

            <div class="project-info">

                <div class="project-name">
                    Diseño Folleto Matrimonio
                </div>

                <div class="project-category">
                    Print
                </div>

            </div>

        </article>


        <!-- PROJECT 04 -->

        <article
            class="project"
            onclick="openProject(
                'Díptico Coloproctólogos Concepción',
                'Diseño editorial · Corporativo',
                'https://www.behance.net/gallery/253653869/PORTFOLIO'
            )"
        >

            <div class="project-image"></div>

            <div class="project-info">

                <div class="project-name">
                    Díptico Coloproctólogos
                </div>

                <div class="project-category">
                    Corporate
                </div>

            </div>

        </article>


        <!-- PROJECT 05 -->

        <article
            class="project"
            onclick="openProject(
                'Diseño de tarjeta de presentación',
                'Branding · Identidad',
                'https://www.behance.net/gallery/253653869/PORTFOLIO'
            )"
        >

            <div class="project-image"></div>

            <div class="project-info">

                <div class="project-name">
                    Tarjeta de Presentación
                </div>

                <div class="project-category">
                    Branding
                </div>

            </div>

        </article>


        <!-- PROJECT 06 -->

        <article
            class="project"
            onclick="openProject(
                'Portafolio Empresa Energías Renovables',
                'Diseño corporativo',
                'https://www.behance.net/gallery/253653869/PORTFOLIO'
            )"
        >

            <div class="project-image"></div>

            <div class="project-info">

                <div class="project-name">
                    Empresa Energías Renovables
                </div>

                <div class="project-category">
                    Corporate
                </div>

            </div>

        </article>


    </div>

</section>


<!-- ========================================
     ABOUT
======================================== -->

<section id="about">

    <div class="section-header">

        <div class="section-number">
            02 / 06
        </div>

        <div class="section-title">
            About Me
        </div>

    </div>


    <div class="about">

        <div>

            <h2>
                Diseño con
                <span>intención.</span>
            </h2>

        </div>


        <div class="about-text">

            <p>
                Soy Paola Cares, diseñadora gráfica
                con experiencia en comunicación visual,
                publicidad, branding y diseño digital.
            </p>

            <p>
                Diseño piezas que buscan resolver una
                necesidad de comunicación sin perder
                personalidad visual.
            </p>


            <div class="skills">

                <div class="skill">Photoshop</div>
                <div class="skill">Illustrator</div>
                <div class="skill">InDesign</div>
                <div class="skill">After Effects</div>
                <div class="skill">Lightroom</div>
                <div class="skill">AI Tools</div>

            </div>

        </div>

    </div>

</section>


<!-- ========================================
     CONTACT
======================================== -->

<section
    id="contact"
    class="contact"
>

    <div class="section-number">
        03 / 06
    </div>

    <h2>
        LET'S<br>
        <span>TALK.</span>
    </h2>


    <a
        href="mailto:paolacares96@gmail.com"
        class="contact-email"
    >
        paolacares96@gmail.com
    </a>


    <div class="socials">

        <a
            href="https://www.behance.net/paolaelizab565"
            target="_blank"
        >
            Behance ↗
        </a>

        <a
            href="https://www.linkedin.com/in/paola-cares-b9aa85338/"
            target="_blank"
        >
            LinkedIn ↗
        </a>

    </div>

</section>

</main>


<!-- ========================================
     FOOTER
======================================== -->

<footer>

    <div>
        PULGA SAD®
    </div>

    <div>
        © 2026 Paola Cares
    </div>

</footer>


<!-- ========================================
     PROJECT MODAL
======================================== -->

<div
    class="modal"
    id="projectModal"
>

    <div class="modal-content">

        <button
            class="modal-close"
            onclick="closeProject()"
        >
            ×
        </button>

        <h2 id="modalTitle">
            Project
        </h2>

        <p id="modalCategory">
            Category
        </p>

        <a
            id="modalLink"
            class="behance-button"
            href="#"
            target="_blank"
        >
            Ver proyecto en Behance ↗
        </a>

    </div>

</div>


<!-- ========================================
     JAVASCRIPT
======================================== -->

<script>

    function openProject(title, category, link) {

        document.getElementById("modalTitle").textContent = title;

        document.getElementById("modalCategory").textContent = category;

        document.getElementById("modalLink").href = link;

        document
            .getElementById("projectModal")
            .classList
            .add("active");
    }


    function closeProject() {

        document
            .getElementById("projectModal")
            .classList
            .remove("active");
    }


    /* Cerrar haciendo click fuera */

    document
        .getElementById("projectModal")
        .addEventListener("click", function(event) {

            if (event.target === this) {
                closeProject();
            }

        });


    /* Cerrar con ESC */

    document.addEventListener("keydown", function(event) {

        if (event.key === "Escape") {
            closeProject();
        }

    });

</script>


</body>
</html>
