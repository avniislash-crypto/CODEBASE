<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title id="page_title">CODEBASE - Yazılım ve Programlama Dilleri</title>
    
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Roboto:wght@300;400&display=swap');

        /* --- TEMEL AYARLAR --- */
        :root {
            --dark-bg: #050510;
            --neon-cyan: #00f3ff;        
            --neon-purple: #bc13fe;     
            --card-border: rgba(188, 19, 254, 0.3);
            --input-bg: #1A1A30; 
        }

        /* GENEL VE ARKA PLAN STİLİ */
        body {
            font-family: 'Roboto', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--dark-bg); 
            color: #ffffff;
            background-image: linear-gradient(rgba(0, 243, 255, 0.05) 1px, transparent 1px),
            linear-gradient(90deg, rgba(0, 243, 255, 0.05) 1px, transparent 1px);
            background-size: 30px 30px;
            min-height: 200vh;
            scroll-behavior: smooth; 
        }
        
        /* AVNİ CİPALOV İMZASI STİLİ */
        .dev-credit {
            font-size: 1rem; 
            color: var(--neon-purple); 
            font-family: 'Orbitron', sans-serif; 
            text-align: center;
            padding-top: 15px;
            text-shadow: 0 0 5px var(--neon-purple);
        }

        /* HEADER & NAVİGASYON */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 40px;
            background: rgba(0,0,0,0.8);
            border-bottom: 1px solid var(--neon-purple);
        }

        .logo {
            font-family: 'Orbitron', sans-serif;
            font-size: 1.5rem;
            color: var(--neon-cyan);
            text-shadow: 0 0 10px var(--neon-cyan);
            font-weight: bold;
        }

        nav {
            text-align: center;
            padding: 20px;
            margin-bottom: 40px;
        }

        nav a {
            color: #e0e0e0;
            margin: 0 15px;
            text-decoration: none;
            font-family: 'Orbitron', sans-serif;
            font-size: 0.9rem;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(--neon-cyan);
            text-shadow: 0 0 8px var(--neon-cyan);
        }

        /* ANA SAYFA ALANI (HERO) */
        .container {
            text-align: center;
            padding: 80px 20px 40px 20px;
            max-width: 800px;
            margin: 0 auto;
        }

        h1 {
            font-family: 'Orbitron', sans-serif;
            font-size: 3rem;
            color: white;
            text-shadow: 0 0 20px var(--neon-purple);
            margin-bottom: 20px;
        }
        
        p {
            font-size: 1.2rem;
            color: #bbbbbb;
            line-height: 1.6;
            margin-bottom: 40px;
        }

        /* CTA BUTONU STİLİ */
        .cta-button {
            padding: 15px 40px;
            background: linear-gradient(90deg, var(--neon-cyan), var(--neon-purple));
            color: black;
            font-weight: bold;
            text-decoration: none;
            border-radius: 30px;
            box-shadow: 0 0 20px rgba(0, 243, 255, 0.5);
            font-family: 'Orbitron', sans-serif;
            display: inline-block;
            transition: 0.3s;
        }

        .cta-button:hover {
            transform: scale(1.05);
            box-shadow: 0 0 40px rgba(188, 19, 254, 0.8);
        }

        /* DİL BUTONLARI STİLİ */
        .language-selector button {
            background: transparent;
            border: 1px solid var(--neon-cyan);
            color: var(--neon-cyan);
            padding: 5px 10px;
            margin-left: 5px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
        }
        .language-selector button:hover {
            background: var(--neon-cyan);
            color: black;
        }

        /* ÖZELLİKLER VE İLETİŞİM GENEL STİLİ */
        .features-section, .contact-section {
            padding: 80px 20px;
            background-color: var(--dark-bg);
            text-align: center;
        }
        
        .features-section h2, .contact-section h2 {
            font-family: 'Orbitron', sans-serif;
            color: var(--neon-cyan);
            text-shadow: 0 0 15px var(--neon-cyan);
            margin-bottom: 60px;
        }

        /* ÖZELLİK KARTLARI (FEATURE CARDS) */
        .feature-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .feature-card {
            background-color: rgba(10, 10, 31, 0.8);
            border: 1px solid var(--card-border);
            border-radius: 10px;
            padding: 30px;
            width: 250px;
            text-align: left;
            box-shadow: 0 0 15px rgba(188, 19, 254, 0.2);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 0 25px rgba(0, 243, 255, 0.6), 0 0 10px rgba(188, 19, 254, 0.8);
        }
        .feature-card h3 {
            color: var(--neon-cyan);
            font-size: 1.2rem;
            border-bottom: 1px solid var(--neon-cyan);
            padding-bottom: 10px;
            margin-top: 0;
            text-shadow: 0 0 5px var(--neon-cyan);
        }
        .feature-card p {
            font-size: 0.9rem;
            color: #bbbbbb;
            margin: 15px 0 0 0;
        }
        
        /* İLETİŞİM FORM STİLİ */
        #contact-form {
            max-width: 600px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        #contact-form input, #contact-form textarea {
            padding: 15px;
            border: 1px solid var(--neon-purple);
            background-color: var(--input-bg);
            color: white; 
            font-size: 1rem;
            border-radius: 5px;
            transition: border-color 0.3s, box-shadow 0.3s;
        }
        
        #contact-form ::placeholder {
            color: #888;
        }


        #contact-form input:focus, #contact-form textarea:focus {
            outline: none;
            border-color: var(--neon-cyan);
            box-shadow: 0 0 10px rgba(0, 243, 255, 0.5);
        }

        #contact-form textarea {
            resize: vertical;
            min-height: 150px;
        }

        #contact-submit {
            cursor: pointer;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="developer_credit" class="dev-credit">Geliştiren: Avni Cipalov</div>

    <header>
        <div class="logo">CODEBASE</div>
        <div class="language-selector">
            <button onclick="changeLanguage('tr')">TR</button>
            <button onclick="changeLanguage('en')">EN</button>
            <button onclick="changeLanguage('de')">DE</button>
            <button onclick="changeLanguage('mk')">MK</button>
        </div>
    </header>

    <nav>
        <a href="#hero" id="nav_home">Ana Sayfa</a>
        <a href="#definition" id="nav_definition">Yazılım Nedir?</a>
        <a href="#languages" id="nav_languages">Programlama Dilleri</a>
        <a href="#contact" id="nav_contact">İletişim</a>
    </nav>

    <div class="container" id="hero">
        <h1 id="hero_headline">KODUN EVRENİNİ<br>KEŞFETMEYE BAŞLA</h1>
        <p id="hero_subtext">Yazılımın temellerinden en popüler programlama dillerinin derinliklerine kadar her şeyi öğrenin. Kodlama yolculuğunuz burada başlıyor.</p>
        <a href="#languages" class="cta-button" id="cta_button">DİLLERE GÖZ ATIN</a>
    </div>
    
    <div class="features-section" id="definition">
        <h2 id="definition_title">YAZILIM NEDİR VE NASIL ÇALIŞIR?</h2>
        <div class="feature-grid">
            <div class="feature-card">
                <h3 id="def1_title">TANIM VE TEMELLER</h3>
                <p id="def1_desc">Yazılım, bilgisayar donanımına belirli görevleri yerine getirmesi için ne yapacağını söyleyen talimatlar ve veriler bütünüdür. İki ana türü vardır: Sistem ve Uygulama.</p>
            </div>
            <div class="feature-card">
                <h3 id="def2_title">NASIL ÇALIŞIR?</h3>
                <p id="def2_desc">Yazılım, yüksek seviyeli dillerle (Python, Java) yazılır, derleyici veya yorumlayıcı tarafından makine diline çevrilir ve donanım üzerinde çalıştırılır.</p>
            </div>
            <div class="feature-card">
                <h3 id="def3_title">MİMARİ VE SÜREÇ</h3>
                <p id="def3_desc">Yazılım Geliştirme Yaşam Döngüsü (SDLC) planlama, analiz, tasarım, uygulama, test ve bakım aşamalarından oluşur.</p>
            </div>
            <div class="feature-card">
                <h3 id="def4_title">GELİŞTİRME ARAÇLARI</h3>
                <p id="def4_desc">VS Code, JetBrains gibi IDE'ler (Entegre Geliştirme Ortamları), kod yazmayı, hata ayıklamayı ve yönetmeyi kolaylaştıran araçlardır.</p>
            </div>
        </div>
    </div>

    <div class="features-section" id="languages">
        <h2 id="languages_title">POPÜLER PROGRAMLAMA DİLLERİNE GİRİŞ</h2>
        <div class="feature-grid">
            <div class="feature-card">
                <h3 id="lang1_title">PYTHON</h3>
                <p id="lang1_desc">Veri bilimi, yapay zeka ve web geliştirme için popüler, okunması ve yazması kolay, çok amaçlı bir dildir.</p>
            </div>
            <div class="feature-card">
                <h3 id="lang2_title">JAVASCRIPT (JS)</h3>
                <p id="lang2_desc">Tüm modern web sitelerinin ön yüzünü (front-end) oluşturur. Node.js ile arka yüzde (back-end) de kullanılır.</p>
            </div>
            <div class="feature-card">
                <h3 id="lang3_title">JAVA</h3>
                <p id="lang3_desc">Büyük ölçekli kurumsal uygulamalar, Android mobil geliştirme ve yüksek performans gerektiren sistemler için idealdir.</p>
            </div>
            <div class="feature-card">
                <h3 id="lang4_title">C#</h3>
                <p id="lang4_desc">Microsoft tarafından geliştirilmiştir. Oyun (Unity), web ve Windows tabanlı masaüstü uygulamaları için kullanılır.</p>
            </div>
        </div>
    </div>

    <div class="contact-section" id="contact">
        <h2 id="contact_title">BİLGİ ALMAK İÇİN BİZE ULAŞIN</h2>
        <form id="contact-form" onsubmit="return false;">
            <input type="text" id="contact_name_input" placeholder="Adınız Soyadınız">
            <input type="email" id="contact_email_input" placeholder="E-posta Adresiniz">
            <textarea id="contact_message_input" placeholder="Yazılım Geliştirme/Dil Sorunuz"></textarea>
            <button type="submit" class="cta-button" id="contact_submit">MESAJI GÖNDER</button>
        </form>
    </div>


    <script>
        const translations = {
            tr: {
                page_title: "CODEBASE - Yazılım ve Programlama Dilleri",
                developer_credit: "Geliştiren: Avni Cipalov",
                nav_home: "Ana Sayfa", nav_definition: "Yazılım Nedir?", nav_languages: "Programlama Dilleri", nav_contact: "İletişim",
                hero_headline: "KODUN EVRENİNİ<br>KEŞFETMEYE BAŞLA",
                hero_subtext: "Yazılımın temellerinden en popüler programlama dillerinin derinliklerine kadar her şeyi öğrenin. Kodlama yolculuğunuz burada başlıyor.",
                cta_button: "DİLLERE GÖZ ATIN",
                
                definition_title: "YAZILIM NEDİR VE NASIL ÇALIŞIR?",
                def1_title: "TANIM VE TEMELLER", def1_desc: "Yazılım, bilgisayar donanımına belirli görevleri yerine getirmesi için ne yapacağını söyleyen talimatlar ve veriler bütünüdür. İki ana türü vardır: Sistem ve Uygulama.",
                def2_title: "NASIL ÇALIŞIR?", def2_desc: "Yazılım, yüksek seviyeli dillerle (Python, Java) yazılır, derleyici veya yorumlayıcı tarafından makine diline çevrilir ve donanım üzerinde çalıştırılır.",
                def3_title: "MİMARİ VE SÜREÇ", def3_desc: "Yazılım Geliştirme Yaşam Döngüsü (SDLC) planlama, analiz, tasarım, uygulama, test ve bakım aşamalarından oluşur.",
                def4_title: "GELİŞTİRME ARAÇLARI", def4_desc: "VS Code, JetBrains gibi IDE'ler (Entegre Geliştirme Ortamları), kod yazmayı, hata ayıklamayı ve yönetmeyi kolaylaştıran araçlardır.",
                
                languages_title: "POPÜLER PROGRAMLAMA DİLLERİNE GİRİŞ",
                lang1_title: "PYTHON", lang1_desc: "Veri bilimi, yapay zeka ve web geliştirme için popüler, okunması ve yazması kolay, çok amaçlı bir dildir.",
                lang2_title: "JAVASCRIPT (JS)", lang2_desc: "Tüm modern web sitelerinin ön yüzünü (front-end) oluşturur. Node.js ile arka yüzde (back-end) de kullanılır.",
                lang3_title: "JAVA", lang3_desc: "Büyük ölçekli kurumsal uygulamalar, Android mobil geliştirme ve yüksek performans gerektiren sistemler için idealdir.",
                lang4_title: "C#", lang4_desc: "Microsoft tarafından geliştirilmiştir. Oyun (Unity), web ve Windows tabanlı masaüstü uygulamaları için kullanılır.",

                contact_title: "BİLGİ ALMAK İÇİN BİZE ULAŞIN",
                contact_name_placeholder: "Adınız Soyadınız",
                contact_email_placeholder: "E-posta Adresiniz",
                contact_message_placeholder: "Yazılım Geliştirme/Dil Sorunuz",
                contact_submit: "MESAJI GÖNDER"
            },
            en: {
                page_title: "CODEBASE - Software and Programming Languages",
                developer_credit: "Developed by: Avni Cipalov",
                nav_home: "Home", nav_definition: "What is Software?", nav_languages: "Programming Languages", nav_contact: "Contact",
                hero_headline: "START EXPLORING<br>THE UNIVERSE OF CODE",
                hero_subtext: "Learn everything from the fundamentals of software to the depths of the most popular programming languages. Your coding journey starts here.",
                cta_button: "EXPLORE LANGUAGES",
                
                definition_title: "WHAT IS SOFTWARE AND HOW DOES IT WORK?",
                def1_title: "DEFINITION AND FUNDAMENTALS", def1_desc: "Software is a set of instructions and data that tells computer hardware what to do to perform specific tasks. There are two main types: System and Application.",
                def2_title: "HOW IT WORKS", def2_desc: "Software is written in high-level languages (Python, Java), translated into machine language by a compiler or interpreter, and executed on the hardware.",
                def3_title: "ARCHITECTURE AND PROCESS", def3_desc: "The Software Development Life Cycle (SDLC) consists of planning, analysis, design, implementation, testing, and maintenance phases.",
                def4_title: "DEVELOPMENT TOOLS", def4_desc: "IDEs (Integrated Development Environments) like VS Code, JetBrains are tools that make writing, debugging, and managing code easier.",
                
                languages_title: "INTRODUCTION TO POPULAR PROGRAMMING LANGUAGES",
                lang1_title: "PYTHON", lang1_desc: "A popular, easy-to-read, and multipurpose language for data science, artificial intelligence, and web development.",
                lang2_title: "JAVASCRIPT (JS)", lang2_desc: "Forms the front-end of all modern websites. Also used on the back-end with Node.js.",
                lang3_title: "JAVA", lang3_desc: "Ideal for large-scale enterprise applications, Android mobile development, and high-performance systems.",
                lang4_title: "C#", lang4_desc: "Developed by Microsoft. Used for gaming (Unity), web, and Windows-based desktop applications.",

                contact_title: "CONTACT US FOR INFORMATION",
                contact_name_placeholder: "Your Name",
                contact_email_placeholder: "Your Email Address",
                contact_message_placeholder: "Your Software Development/Language Question",
                contact_submit: "SEND MESSAGE"
            },
            de: {
                page_title: "CODEBASE - Software und Programmiersprachen",
                developer_credit: "Entwickelt von: Avni Cipalov",
                nav_home: "Startseite", nav_definition: "Was ist Software?", nav_languages: "Programmiersprachen", nav_contact: "Kontakt",
                hero_headline: "STARTEN SIE DIE ERFORSCHUNG<br>DES UNIVERSUMS DES CODES",
                hero_subtext: "Lernen Sie alles, von den Grundlagen der Software bis in die Tiefen der beliebtesten Programmiersprachen. Ihre Codierungsreise beginnt hier.",
                cta_button: "SPRACHEN ENTDECKEN",
                
                definition_title: "WAS IST SOFTWARE UND WIE FUNKTIONIERT SIE?",
                def1_title: "DEFINITION UND GRUNDLAGEN", def1_desc: "Software ist eine Reihe von Anweisungen und Daten, die der Computerhardware mitteilen, was zu tun ist, um bestimmte Aufgaben auszuführen. Es gibt zwei Haupttypen: System und Anwendung.",
                def2_title: "WIE ES FUNKTIONIERT", def2_desc: "Software wird in höheren Sprachen (Python, Java) geschrieben, von einem Compiler oder Interpreter in Maschinensprache übersetzt und auf der Hardware ausgeführt.",
                def3_title: "ARCHITEKTUR UND PROZESS", def3_desc: "Der Softwareentwicklungs-Lebenszyklus (SDLC) besteht aus den Phasen Planung, Analyse, Design, Implementierung, Test und Wartung.",
                def4_title: "ENTWICKLUNGSTOOLS", def4_desc: "IDEs (Integrated Development Environments) wie VS Code, JetBrains sind Tools, die das Schreiben, Debuggen und Verwalten von Code erleichtern.",

                languages_title: "EINFÜHRUNG IN BELIEBTE PROGRAMMIERSPRACHEN",
                lang1_title: "PYTHON", lang1_desc: "Eine beliebte, leicht lesbare und vielseitige Sprache für Data Science, KI und Webentwicklung.",
                lang2_title: "JAVASCRIPT (JS)", lang2_desc: "Bildet das Front-End aller modernen Websites. Wird mit Node.js auch im Back-End verwendet.",
                lang3_title: "JAVA", lang3_desc: "Ideal für große Unternehmensanwendungen, Android-Mobilentwicklung und Hochleistungssysteme.",
                lang4_title: "C#", lang4_desc: "Von Microsoft entwickelt. Wird für Spiele (Unity), Web- und Windows-basierte Desktop-Anwendungen verwendet.",

                contact_title: "KONTAKTIEREN SIE UNS FÜR INFORMATIONEN",
                contact_name_placeholder: "Ihr Name",
                contact_email_placeholder: "Ihre E-Mail-Adresse",
                contact_message_placeholder: "Ihre Frage zur Softwareentwicklung/Sprache",
                contact_submit: "NACHRICHT SENDEN"
            },
            mk: {
                page_title: "CODEBASE - Софтвер и Програмски Јазици",
                developer_credit: "Развиено од: Avni Cipalov",
                nav_home: "Почетна", nav_definition: "Што е Софтвер?", nav_languages: "Програмски Јазици", nav_contact: "Контакт",
                hero_headline: "ЗАПОЧНЕТЕ СО ИСТРАЖУВАЊЕ<br>НА УНИВЕРЗУМОТ НА КОДОТ",
                hero_subtext: "Научете сè, од основите на софтверот до длабочините на најпопуларните програмски јазици. Вашето кодирање патување започнува тука.",
                cta_button: "ИСТРАЖЕТЕ ЈАЗИЦИ",

                definition_title: "ШТО Е СОФТВЕР И КАКО РАБОТИ?",
                def1_title: "ДЕФИНИЦИЈА И ОСНОВИ", def1_desc: "Софтверот е збир на инструкции и податоци кои му кажуваат на компјутерскиот хардвер што да прави за да изврши одредени задачи. Постојат два главни типа: Системски и Апликативен.",
                def2_title: "КАКО РАБОТИ", def2_desc: "Софтверот е напишан во јазици од високо ниво (Python, Java), преведен на машински јазик од компајлер или интерпретатор, и извршен на хардверот.",
                def3_title: "АРХИТЕКТУРА И ПРОЦЕС", def3_desc: "Животниот циклус на развој на софтвер (SDLC) се состои од фази на планирање, анализа, дизајн, имплементација, тестирање и одржување.",
                def4_title: "АЛАТКИ ЗА РАЗВОЈ", def4_desc: "IDE-и (Интегрирани развојни околини) како VS Code, JetBrains се алатки кои го олеснуваат пишувањето, дебагирањето и управувањето со кодот.",
                
                languages_title: "ВОВЕД ВО ПОПУЛАРНИТЕ ПРОГРАМСКИ ЈАЗИЦИ",
                lang1_title: "PYTHON", lang1_desc: "Популарен, лесен за читање и повеќенаменски јазик за наука за податоци, вештачка интелигенција и веб развој.",
                lang2_title: "JAVASCRIPT (JS)", lang2_desc: "Ја формира предната страна (front-end) на сите модерни веб-страници. Се користи и на задната страна (back-end) со Node.js.",
                lang3_title: "JAVA", lang3_desc: "Идеален за големи корпоративни апликации, развој на Android мобилни уреди и системи кои бараат високи перформанси.",
                lang4_title: "C#", lang4_desc: "Развиен од Microsoft. Се користи за игри (Unity), веб и десктоп апликации базирани на Windows.",
                
                contact_title: "КОНТАКТИРАЈТЕ НЕ ЗА ИНФОРМАЦИИ",
                contact_name_placeholder: "Вашето име",
                contact_email_placeholder: "Вашата е-пошта адреса",
                contact_message_placeholder: "Вашето прашање за развој на софтвер/јазик",
                contact_submit: "ИСПРАТИ ПОРАКА"
            }
        };

        // GÜVENİLİR VE HATA TOLERANSLI DİL ÇEVİRİ FONKSİYONU
        function changeLanguage(lang) {
            const data = translations[lang];
            
            for (const key in data) {
                // 1. Sayfa Başlığını Güncelle
                if (key === 'page_title') {
                    document.title = data[key];
                    continue; 
                }

                // 2. Placeholder Metinlerini Güncelle
                if (key.endsWith('_placeholder')) {
                    const targetId = key.replace('_placeholder', '_input');
                    const targetElement = document.getElementById(targetId);
                    if (targetElement) { 
                         targetElement.placeholder = data[key];
                    }
                    continue;
                }

                // 3. Normal Metinleri Güncelle (header ve butonlar dahil)
                const element = document.getElementById(key);

                if (element) {
                    if (key.endsWith('_headline')) { // Başlıklar için innerHTML (br etiketi içerir)
                        element.innerHTML = data[key]; 
                    } else {
                        element.innerText = data[key]; // Diğer metinler için innerText
                    }
                } 
            }

            document.documentElement.lang = lang; 
        }

        // Sayfa yüklendiğinde varsayılan dil Türkçe
        changeLanguage('tr'); 
    </script>

</body>
</html>
