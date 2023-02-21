# codetribe.javascript
<!DOCTYPE html>
<html>
    <head>
        <title>My Webpage</title>
    </head>
    <body>
        <header>
            <h1>About Me</h1>
        </header>
        <main>
            <section>
                <h2>Personal Information</h2>
                <p>Name: <span id="name"></span></p>
                <p>Age: <span id="age"></span></p>
                <p>Location: <span id="location"></span></p>
            </section>
            <section>
                <h2>Educational Background</h2>
                <p id="edu-line-1"></p>
            </section>
            <section>
                <h2>Projects</h2>
                <ul>
                    <li id="projects-line-1"></li>
                    <li id="projects-line-2"></li>
                </ul>
            </section>
            <section>
                <h2>Work Experience</h2>
                <p id="work-line-1"></p>
            </section>
            <section>
                <h2>Skills and Expertise</h2>
                <ul>
                    <li id="skills-line-1"></li>
                    <li id="skills-line-2"></li>
                </ul>
            </section>
            <section>
                <h2>Interests and Hobbies</h2>
                <p id="interests-line-1"></p>
            </section>
        </main>

        <script>
            const info = {
                personal: [
                    { id: 'name', value: 'Kate Maakane' },
                    { id: 'age', value: '25' },
                    { id: 'location', value: '10925 isitulo street Vosloorus 1475' },
                ],
                education: [
                    { id: 'edu-line-1', value: 'Software Development Diploma at Tshwane University of Technology' }
                ],
                projects: [
                    { id: 'projects-line-1', value: 'Developed a mobile app for Final year Project at Tshwane University of Technology' },
                    { id: 'projects-line-2', value: 'Created a website for a local non-profit organization' },
                ],
                work: [
                    { id: 'work-line-1', value: 'Software Engineer Freelancer  (2020-present)' }
                ],
                skills: [
                    { id: 'skills-line-1', value: 'Programming languages:C++, HTML,SQL noSQL' },
                    { id: 'skills-line-2', value: 'Web development frameworks: React, Angular' }
                ],
                interests: [
                    { id: 'interests-line-1', value: 'Coding, Exercising, Cooking' }
                ]
            }

            for (key in info) {
                if (!info.hasOwnProperty(key)) continue;

                info[key].forEach(({id, value}) => {
                    document.getElementById(id).innerText = value
                })
            }
        </script>
    </body>
</html>
