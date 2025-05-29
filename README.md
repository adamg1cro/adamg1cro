<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adam Green - CRO Specialist</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Application Structure Plan: 
        The SPA is structured as a single, scrollable page with a fixed top navigation bar for quick access to key sections. 
        Sections include:
        1. Hero: Name, tagline, and primary contact.
        2. Summary: Detailed professional statement.
        3. Experience: Chronologically listed roles, with interactive cards/accordions to expand and view detailed responsibilities and achievements. This approach allows for a clean initial view while providing depth on demand.
        4. Education: Clearly presented qualifications.
        5. Skills: Categorized technical and soft skills presented as visually distinct tags for quick scanning.
        6. Contact: Footer with contact information and links.
        This structure was chosen for its intuitive flow, mirroring how a CV is typically read, while enhancing it with interactivity for better engagement and information digestion. The progressive disclosure of information in the 'Experience' section prevents overwhelming the user.
    -->
    <!-- Visualization & Content Choices: 
        Report Info: Adam Green's CV text.
        Goal: Present a professional profile in an interactive, engaging, and easily consumable manner.
        Viz/Presentation Method:
            - Hero: Large heading for name, prominent tagline.
            - Summary: Well-formatted text block.
            - Experience: Interactive cards using HTML/Tailwind, JS for expand/collapse. Each card details a role.
            - Education: Structured list.
            - Skills: Visually distinct tags for each skill, grouped by category.
        Interaction:
            - Smooth scrolling for navigation links.
            - Click to expand/collapse job details in the Experience section.
        Justification: 
            - The chosen methods prioritize clarity, readability, and professional aesthetics suitable for a CV. 
            - Interactive elements encourage exploration without cluttering the initial view. 
            - Tag-based skill presentation allows for quick assessment of competencies.
        Library/Method: HTML, Tailwind CSS for layout and styling, Vanilla JavaScript for interactions.
    -->
    <style>
        body {
            font-family: 'Inter', sans-serif; /* Fallback font, assuming Inter is loaded or preferred */
        }
        /* Smooth scrolling */
        html {
            scroll-behavior: smooth;
        }
        .active-nav {
            color: #0D9488; /* teal-600 */
            font-weight: 600;
        }
        .experience-card ul {
            list-style-type: disc;
            padding-left: 1.5rem;
        }
        .skill-tag {
            transition: all 0.2s ease-in-out;
        }
        .skill-tag:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
        }
    </style>
    <link rel="preconnect" href="https://rsms.me/">
    <link rel="stylesheet" href="https://rsms.me/inter/inter.css">
</head>
<body class="bg-stone-50 text-stone-800 antialiased">

    <header class="bg-stone-100/80 backdrop-blur-md shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#hero" class="text-2xl font-bold text-teal-700 hover:text-teal-600 transition-colors">Adam Green</a>
            <div class="space-x-4 md:space-x-6 text-sm md:text-base">
                <a href="#summary" class="text-stone-600 hover:text-teal-600 transition-colors nav-link">Summary</a>
                <a href="#experience" class="text-stone-600 hover:text-teal-600 transition-colors nav-link">Experience</a>
                <a href="#education" class="text-stone-600 hover:text-teal-600 transition-colors nav-link">Education</a>
                <a href="#skills" class="text-stone-600 hover:text-teal-600 transition-colors nav-link">Skills</a>
                <a href="#contact" class="text-stone-600 hover:text-teal-600 transition-colors nav-link">Contact</a>
            </div>
        </nav>
    </header>

    <main class="container mx-auto px-6 py-8 md:py-12">

        <section id="hero" class="min-h-[60vh] flex flex-col justify-center items-center text-center py-16 md:py-24">
            <h1 class="text-5xl md:text-7xl font-extrabold mb-4 text-teal-700">Adam Green</h1>
            <p class="text-xl md:text-2xl text-stone-600 mb-8 max-w-3xl">
                Conversion Rate Optimisation Specialist | Driving Growth Through Data-Driven UX & Persuasion Science
            </p>
            <a href="mailto:adamgreenedits.1@gmail.com" class="bg-teal-600 hover:bg-teal-700 text-white font-semibold py-3 px-8 rounded-lg shadow-md hover:shadow-lg transition-all duration-300">
                Get In Touch
            </a>
        </section>

        <section id="summary" class="py-12 md:py-20 scroll-mt-20">
            <h2 class="text-3xl md:text-4xl font-bold mb-8 text-center text-teal-700">Professional Summary</h2>
            <div class="bg-white p-8 rounded-xl shadow-lg max-w-3xl mx-auto">
                <p class="text-lg text-stone-700 leading-relaxed">
                    Highly accomplished and results-driven Conversion Rate Optimisation Specialist with over 3 years of hands-on experience in e-commerce and D2C environments, consistently driving measurable CRO and analytics improvements across multi-million-dollar revenue funnels. Possessing advanced proficiency in web analytics (Google Analytics 4) and a deep understanding of UX/UI design principles, I excel at transforming complex data into actionable insights and strategic optimization roadmaps. My expertise extends to specialized CRO principles, including the application of Cialdini's principles of persuasion and Neurodesign sciences, enabling me to architect conversion excellence and deliver significant ROI improvements through innovative A/B and multivariate testing.
                </p>
            </div>
        </section>

        <section id="experience" class="py-12 md:py-20 scroll-mt-20">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center text-teal-700">Work Experience</h2>
            <div class="max-w-4xl mx-auto space-y-10">
                <p class="text-center text-stone-600 mb-10 text-lg">
                    This section outlines my professional journey, detailing my roles and key contributions. Click on each role to see more specific achievements and responsibilities, showcasing how I've applied my CRO and marketing expertise to drive results.
                </p>
                
                <div class="bg-white p-6 md:p-8 rounded-xl shadow-lg experience-card">
                    <button class="w-full text-left focus:outline-none" onclick="toggleExperience(this)">
                        <div class="flex justify-between items-center mb-2">
                            <h3 class="text-xl md:text-2xl font-semibold text-teal-600">Conversion Rate Optimisation Manager</h3>
                            <span class="text-teal-500 transform transition-transform duration-300">▼</span>
                        </div>
                        <p class="text-stone-600 text-sm md:text-base"><strong>Travel Chapter</strong> | Bideford, UK</p>
                        <p class="text-stone-500 text-xs md:text-sm">July 2024 – Present</p>
                    </button>
                    <div class="mt-4 experience-details hidden pl-4 border-l-2 border-teal-200">
                        <ul class="space-y-2 text-stone-700 leading-relaxed">
                            <li><strong>Strategic CRO Program Leadership:</strong> Spearheaded all Conversion Rate Optimisation (CRO) activities following a structured flywheel process, integrating comprehensive quantitative and qualitative insights to identify critical bottlenecks and opportunities across core user journeys.</li>
                            <li><strong>Data-Driven Opportunity Identification:</strong> Utilized GA4 data to pinpoint conversion roadblocks and accurately forecast potential revenue gains (weekly, monthly, quarterly, annually) based on projected uplift throughout the conversion funnel, directly informing business strategy and investment.</li>
                            <li><strong>Advanced Qualitative Research & Analysis:</strong> Conducted in-depth behavioral analysis using tools like Crazy Egg (heatmapping, session recordings, click maps, user surveys). Designed and executed B2C (holiday bookers) and B2B (property managers) moderated user studies, including competitive benchmarking, to gather rich, actionable insights.</li>
                            <li><strong>Insight Prioritization & Hypothesization:</strong> Leveraged SurveyMonkey to quantify qualitative findings and perform sentiment analysis, systematically prioritizing insights into key themes. Collaborated closely with stakeholders to develop robust testing hypotheses and provide transparent reporting on CRO program performance, including test volume, win rate, loss prevention learnings, and implementation success.</li>
                            <li><strong>Innovative Testing Methodologies & Statistical Rigor:</strong> Navigated technical constraints by implementing unconventional product targeting strategies due to limitations with traditional client-side testing and server-side development resources. Developed a custom formula for attributing desirability scores to properties, ensuring statistical validity and balanced A/A test groups (p-value 0.01) prior to trial launch.</li>
                            <li><strong>A/B Test Configuration & Execution:</strong> Applied a rigorous prioritization framework (effort, impact, confidence, business considerations) to A/B tests, configuring experiments for minimal duration and maximum velocity. Proficiently executed diverse test types including A/B/n, Multi-Armed Bandit (MAB), Multivariate (MVT), and Split URL tests.</li>
                            <li><strong>Comprehensive Statistical Analysis & Validation:</strong> Employed a range of statistical models (CUPED, Bayesian, Frequentist, Z-tests – one-sided/two-sided) for robust analysis. Ensured all tests met a minimum statistical significance of 95% (with higher thresholds for critical booking funnel and checkout stages) and a power value of 80%. Applied Bonferroni correction or False Discovery Rate (FDR) to control for multiple comparisons in non-traditional product testing.</li>
                            <li><strong>Cross-functional Collaboration & High Implementation Rate:</strong> Communicated detailed test plans and high-fidelity UX mock-ups to stakeholders and relevant heads of department, fostering strong cross-functional alignment. This collaborative approach ensured new web components did not negatively impact other operations, contributing to an impressive implementation rate exceeding 90%. Collaborated with product development teams on server-side testing utilizing tools such as Converge Experiences, Mida, and A/B Tasty.</li>
                        </ul>
                    </div>
                </div>

                <div class="bg-white p-6 md:p-8 rounded-xl shadow-lg experience-card">
                    <button class="w-full text-left focus:outline-none" onclick="toggleExperience(this)">
                        <div class="flex justify-between items-center mb-2">
                            <h3 class="text-xl md:text-2xl font-semibold text-teal-600">Marketing Specialist</h3>
                            <span class="text-teal-500 transform transition-transform duration-300">▼</span>
                        </div>
                        <p class="text-stone-600 text-sm md:text-base"><strong>Everything Managed</strong> | Newcastle, UK</p>
                        <p class="text-stone-500 text-xs md:text-sm">May 2022 – July 2024</p>
                    </button>
                    <div class="mt-4 experience-details hidden pl-4 border-l-2 border-teal-200">
                        <ul class="space-y-2 text-stone-700 leading-relaxed">
                            <li><strong>User Experience & Conversion Rate Optimization Leadership:</strong> Took complete ownership of on-site conversion rates (CRO) and user experience (UX) across a portfolio of SME-focused utility and services websites, serving as the primary driver of optimization initiatives and accountable for measurable improvements within a multi-million-dollar revenue funnel.</li>
                            <li><strong>Strategic Optimization & Data-Driven Innovation:</strong> Architected and executed comprehensive optimization strategies, leveraging both qualitative methods (UX principles, site reviews) and quantitative insights (web analytics, traffic analysis) to drive sustainable performance improvements. Led internal planning and oversaw the development of A/B and multivariate testing roadmaps that delivered significant conversion lifts across key funnels and touchpoints.</li>
                            <li><strong>Growth Opportunity Identification & Analysis:</strong> Identified high-impact CRO and UX growth opportunities by conducting in-depth analysis of site usage trends, synthesizing insights from quantitative data, consumer feedback, and usability studies.</li>
                            <li><strong>Cross-functional Collaboration & Stakeholder Management:</strong> Collaborated extensively with stakeholders and heads of department, particularly within finance brands, to ensure alignment on UX and CRO initiatives. Utilized utilities as a primary client acquisition channel, subsequently enabling effective cross-selling of other relevant products.</li>
                            <li><strong>Executive Reporting & Insight Delivery:</strong> Produced high-quality strategy decks, creative briefs, and detailed weekly/monthly performance reports, providing executive-level insights to support senior leadership decision-making and foster cross-functional alignment.</li>
                            <li><strong>Testing Integrity & Documentation:</strong> Ensured the integrity and accuracy of all testing initiatives by troubleshooting test configurations, identifying issues in setups, and delivering clear internal and external documentation to effectively communicate results and learnings.</li>
                            <li><strong>Team Development & Mentorship:</strong> Contributed to team development by training and guiding members on advanced conversion optimization practices, fostering a culture of analytical excellence and continuous improvement within the marketing function.</li>
                        </ul>
                    </div>
                </div>

                <div class="bg-white p-6 md:p-8 rounded-xl shadow-lg experience-card">
                    <button class="w-full text-left focus:outline-none" onclick="toggleExperience(this)">
                         <div class="flex justify-between items-center mb-2">
                            <h3 class="text-xl md:text-2xl font-semibold text-teal-600">SEO & CRO Specialist (Part-time)</h3>
                            <span class="text-teal-500 transform transition-transform duration-300">▼</span>
                        </div>
                        <p class="text-stone-600 text-sm md:text-base"><strong>Revgear</strong> | UK</p>
                        <p class="text-stone-500 text-xs md:text-sm">Jan 2023 – Mar 2024</p>
                    </button>
                    <div class="mt-4 experience-details hidden pl-4 border-l-2 border-teal-200">
                        <ul class="space-y-2 text-stone-700 leading-relaxed">
                            <li><strong>Comprehensive SEO Strategy & Execution:</strong> Developed and implemented robust SEO strategies, encompassing content writing, technical SEO auditing, and on-page optimization, significantly enhancing organic search visibility and performance for multiple UK-based brands.</li>
                            <li><strong>AI Optimization for Search:</strong> Optimized digital content and technical SEO elements for compatibility with emerging AI search algorithms, ensuring future-proofed search engine rankings.</li>
                            <li><strong>Digital Acquisition Channel Management:</strong> Managed and optimized diverse digital acquisition channels, including email marketing, Pay-Per-Click (PPC) campaigns, SEO, and social media advertising, to drive traffic and conversions.</li>
                            <li><strong>Conversion Rate Optimization (CRO):</strong> Applied CRO principles to improve user experience and conversion funnels, working to translate increased traffic into measurable business outcomes.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section id="education" class="py-12 md:py-20 bg-stone-100 scroll-mt-20">
            <div class="max-w-4xl mx-auto px-6">
                <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center text-teal-700">Education & Certifications</h2>
                 <p class="text-center text-stone-600 mb-10 text-lg">
                    My formal education and specialized certifications form the foundation of my expertise in marketing, web design, and conversion optimization. This section highlights key qualifications that equip me with theoretical knowledge and practical skills.
                </p>
                <div class="grid md:grid-cols-3 gap-8 text-center">
                    <div class="bg-white p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-semibold text-teal-600 mb-2">Conversion Rate Optimisation - Minidegree</h3>
                        <p class="text-stone-600">CXL</p>
                        <p class="text-stone-500 text-sm">2023</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-semibold text-teal-600 mb-2">Web Design - Nanodegree</h3>
                        <p class="text-stone-600">Udacity</p>
                        <p class="text-stone-500 text-sm">[Year of Completion]</p>
                    </div>
                    <div class="bg-white p-6 rounded-xl shadow-lg">
                        <h3 class="text-xl font-semibold text-teal-600 mb-2">BA in Russian and German</h3>
                        <p class="text-stone-600">The University of Nottingham</p>
                        <p class="text-stone-500 text-sm">2014</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="skills" class="py-12 md:py-20 scroll-mt-20">
            <div class="max-w-5xl mx-auto px-6">
                <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center text-teal-700">Skills</h2>
                 <p class="text-center text-stone-600 mb-10 text-lg">
                    Here's a snapshot of my technical and soft skills. These competencies are crucial for my role in CRO, enabling me to analyze data, design effective tests, collaborate with teams, and drive strategic initiatives.
                </p>
                <div class="grid md:grid-cols-2 gap-x-12 gap-y-8">
                    <div>
                        <h3 class="text-2xl font-semibold text-teal-600 mb-6">Technical Skills</h3>
                        <div class="flex flex-wrap gap-3">
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">CRO</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">UX Design Principles</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">A/B & MVT Testing</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Google Analytics 4</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Crazy Egg</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">SurveyMonkey</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Statistical Analysis</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">A/B Testing Tools</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">SEO</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Technical SEO</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Content Writing</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">AI Search Optimization</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Digital Marketing</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Email Marketing</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">PPC Advertising</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Social Media Ads</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Web Analytics</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">UX Mock-ups</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Data Analysis</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Funnel Analysis</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Hypothesis Generation</span>
                            <span class="skill-tag bg-teal-100 text-teal-700 px-4 py-2 rounded-full text-sm font-medium">Experiment Design</span>
                        </div>
                    </div>
                    <div>
                        <h3 class="text-2xl font-semibold text-teal-600 mb-6">Soft Skills</h3>
                        <div class="flex flex-wrap gap-3">
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Strategic Planning</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Collaboration</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Stakeholder Management</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Problem-Solving</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Data-Driven Decisions</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Analytical Thinking</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Communication</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Presentation Skills</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Mentorship</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Prioritization</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Attention to Detail</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Adaptability</span>
                            <span class="skill-tag bg-sky-100 text-sky-700 px-4 py-2 rounded-full text-sm font-medium">Results-Oriented</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer id="contact" class="bg-stone-800 text-stone-300 py-12 scroll-mt-20">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-2xl md:text-3xl font-bold mb-6 text-teal-400">Let's Connect</h2>
            <p class="mb-2 text-lg">Adam Green</p>
            <p class="mb-2"><a href="mailto:adamgreenedits.1@gmail.com" class="hover:text-teal-400 transition-colors">adamgreenedits.1@gmail.com</a></p>
            <p class="mb-6">Bideford, UK</p>
            <p class="text-sm">&copy; <span id="currentYear"></span> Adam Green. All rights reserved.</p>
        </div>
    </footer>

    <script>
        function toggleExperience(buttonElement) {
            const details = buttonElement.nextElementSibling;
            const arrow = buttonElement.querySelector('span');
            if (details.classList.contains('hidden')) {
                details.classList.remove('hidden');
                arrow.style.transform = 'rotate(180deg)';
            } else {
                details.classList.add('hidden');
                arrow.style.transform = 'rotate(0deg)';
            }
        }

        document.getElementById('currentYear').textContent = new Date().getFullYear();
        
        const navLinks = document.querySelectorAll('.nav-link');
        const sections = document.querySelectorAll('main section');

        function changeNavActiveState() {
            let index = sections.length;

            while(--index && window.scrollY + 100 < sections[index].offsetTop) {}
            
            navLinks.forEach((link) => link.classList.remove('active-nav'));
            if (index >= 0 && navLinks[index]) {
                 navLinks[index].classList.add('active-nav');
            }
        }

        changeNavActiveState();
        window.addEventListener('scroll', changeNavActiveState);

    </script>
</body>
</html>
```
