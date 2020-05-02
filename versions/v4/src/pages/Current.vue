<template>
  <div class="website">
		<div class="sidebar">

			<div class="sidebar__wrapper">
				<div class="sidebar__photo">
					<img class="sidebar__photo__img" src="@/assets/current/photo.jpeg" />
				</div>

				<div class="sidebar__heading">
					<h1 class="sidebar__heading__name">Jieun Lee</h1>
				</div>

				<div class="sidebar__description">
					<p>
						Combined Major in Computer Science and Mathematics at UBC
					</p>
				</div>

				<div class="sidebar__menu">
					<div class="sidebar__menu__item">
						<a href="#about">About Me</a>
					</div>
					<div class="sidebar__menu__item">
						<a href="#skills">Skills</a>
					</div>
					<div class="sidebar__menu__item">
						<a href="#projects">Projects</a>
					</div>
					<div class="sidebar__menu__item">
						<a href="#interests">Interests</a>
					</div>
					<div class="sidebar__menu__item">
						<a href="#contact">More Info</a>
					</div>
				</div>

				<div class="sidebar__links">
					<a href="https://github.com/jieun-lee" target="_blank">
						<img src="@/assets/current/icons/github.png" alt="GitHub"/>
					</a>
					<a href="https://jieun-lee.myportfolio.com/" target="_blank">
						<img src="@/assets/current/icons/portfolio.png" alt="MyPortfolio"/>
					</a>
					<a href="https://www.linkedin.com/in/jieun-leee" target="_blank">
						<img src="@/assets/current/icons/linkedin.png" alt="LinkedIn"/>
					</a>
				</div>
			</div>
		</div><div class="main">

			<div class="section section__about" id="about">
				<div class="section--header">
					About Me
				</div>

				<div class="section--body">
					<p>
						Hello! I'm a software developer based in Vancouver, BC.
						I recently completed my Bachelor of Science in Computer Science and Mathematics at <a href="https://www.ubc.ca" target="_blank">UBC</a>.
						Previously, I worked as a co-op software developer at
						<a href="https://hootsuite.com/" target="_blank">Hootsuite</a>
						and at
						<a href="https://www.sap.com/canada/index.html" target="_blank">SAP</a>.
					</p>
					<p>
						My greatest programming interests lie in web development, utilizing JavaScript, HTML, CSS, as well as other frameworks and libraries such as React
						and Vue.js to implement beautiful and intuitive web interfaces. In addition to my co-op experiences that both made use of these technologies, I worked on
						several academic and <a href="https://github.com/jieun-lee" target="_blank">personal projects</a> through which I have elevated my skills.
					</p>
					<p>
						I also enjoy programming in Java, which was the first official programming language I had worked with.
						I am also interested in learning more about mobile development; I worked on some projects with React Native, and also with Java and XML through Android Studio.
					</p>
					<p>
						Outside of my programming life, I have a passion for music and playing instruments.
						I started playing piano since I was young, and picked up guitar a couple years ago as well.
						I enjoy both playing alone or as part of a band.
						Occasionally I am also a hobbyist <a href="https://jieun-lee.myportfolio.com/" target="_blank">photographer</a>.
					</p>
				</div>
			</div>

			<div class="section section__skills" id="skills">
				<div class="section--header">
					Skills
				</div>

				<div class="section--body">
					Programming:
					<ul>
						<li>Java</li>
						<li>TypeScript</li>
						<li>React Native</li>
						<li>Python</li>
					</ul><br>

					Web Development:
					<ul>
						<li>JavaScript</li>
						<li>CSS/SASS</li>
						<li>HTML</li>
						<li>PHP</li>
						<li>Node.js</li>
					</ul><br>

					Libraries/Frameworks:
					<ul>
						<li>React</li>
						<li>Vue.js</li>
						<li>jQuery</li>
						<li>Jasmine</li>
						<li>Twig</li>
					</ul><br>

					Other:
					<ul>
						<li>SQL</li>
						<li>Git</li>
						<li>XML</li>
						<li>JSON</li>
						<li>ThreeJS</li>
						<li>Matlab</li>
						<li>LaTeX</li>
						<li>Photoshop</li>
					</ul>
				</div>
			</div>

			<div class="section section__projects" id="projects">
				<div class="section--header">
					Featured Projects
				</div>

				<div class="section--body">

					<div class="project__item">
						<div class="project__item__title">
						Mini Drum Kit <span style="font-size: 14px; color: #676767;">(in progress)</span>
						</div>
						<div class="project__item__skills">
							HTML, CSS, JavaScript, Vue.js
						</div>
						<div class="project__item__description">
							In-browser drum kit with a basic Kick, Snare, Hi-Hat, and Crash (sounds from Focusrite)
						</div>
						<div class="project__item__link">
							See on <a href="https://github.com/jieun-lee/mini-drum-kit">Github</a> or try it out
							<a href="https://jieun-lee.github.io/mini-drum-kit/">Here</a>
						</div>
					</div>

					<div class="project__item">
						<div class="project__item__title">
							Type the Food
						</div>
						<div class="project__item__skills">
							HTML, CSS, JavaScript
						</div>
						<div class="project__item__description">
							Mini browser game involving memorizing short menus and typing
						</div>
						<div class="project__item__link">
							See on <a href="https://github.com/jieun-lee/type-the-food">Github</a> or try it out
							<a href="https://jieun-lee.github.io/type-the-food/">Here</a>
						</div>
					</div>

					<div class="project__item">
						<div class="project__item__title">
							Ice Cream Game
						</div>
						<div class="project__item__skills">
							Java, Java Swing
						</div>
						<div class="project__item__description">
							Original Monopoly-like board game<br>
							Two players move around the board, buying ice cream flavours and collecting stars
						</div>
						<div class="project__item__link">
							See on <a href="https://github.com/jieun-lee/ice-cream-game">Github</a>
						</div>
					</div>

					<div class="project__item">
						<div class="project__item__title">
							Cookbook Database
						</div>
						<div class="project__item__skills">
							PHP, Javascript, SQL, CSS, HTML
						</div>
						<div class="project__item__description">
							Group project for a databases course at school<br>
							A recipe database where users can upload their own recipes and manage their own cookbooks
						</div>
						<div class="project__item__link">
							See on <a href="https://github.com/soohyunkim/Cookbook">Github</a>
						</div>
					</div>

					<div class="project__item">
						<div class="project__item__title">
							Flying Vegetable Mini Game
						</div>
						<div class="project__item__skills">
							Version 1: Java, Java Swing<br>
							Version 2: JavaScript, HTML Canvas
						</div>
						<div class="project__item__description">
							Mini game where a vegetable files up and down to avoid hitting obstacles
						</div>
						<div class="project__item__link">
							See on <a href="https://github.com/jieun-lee/fly-vegetable">Github</a> or try it out
							<a href="https://jieun-lee.github.io/fly-vegetable/JavaScript/main.html">Here</a>
						</div>
					</div>

				</div>
			</div>

			<div class="section section__interests" id="interests">
				<div class="section--header">
					Interests
				</div>

				<div class="section--body">
					Some of my interests include:
					<ul>
						<li>Programming</li>
						<li>Music</li>
						<li>Photography</li>
					</ul>
				</div>
			</div>

			<div class="section section__contact" id="contact">
				<div class="section--header">
					More Info
				</div>

				<div class="section--body">
					View my projects and code on <a href="https://github.com/jieun-lee" target="_blank">Github</a><br>
					View some of my photography on <a href="https://jieun-lee.myportfolio.com/" target="_blank">MyPortfolio</a><br>
					Connect with me on <a href="https://www.linkedin.com/in/jieun-leee" target="_blank">LinkedIn</a>
				</div>
			</div>

		</div>
	</div>
</template>

<style scoped>
.website {
  flex-direction: column; }
  @media (min-width: 768px) {
    .website {
      flex-direction: row; } }

@media (min-width: 768px) and (max-width: 1023px) {
  .sidebar__wrapper {
    position: fixed;
    width: 33%; } }
@media (min-width: 1024px) {
  .sidebar__wrapper {
    position: fixed;
    width: 28%; } }
@media (min-width: 768px) and (max-width: 1023px) {
  .sidebar {
    width: 33%; } }
@media (min-width: 1024px) {
  .sidebar {
    width: 28%; } }

@media (min-width: 768px) and (max-width: 1023px) {
  .main {
    width: 67%; } }
@media (min-width: 1024px) {
  .main {
    width: 72%; } }

.website {
  font-family: "Source Sans Pro", sans-serif;
  margin: 0;
  display: flex;
  /* to fit page after making it a Vue component */
  position: absolute;
  top: 0;
  left: 0; }

.sidebar {
  text-align: center;
  z-index: 1;
  background-color: #b2c2d4;
  box-shadow: 1px 0px 20px -2px rgba(0, 0, 0, 0.3); }
  .sidebar__wrapper > div {
    margin: 24px; }
  .sidebar__photo {
    margin: 24px auto !important;
    width: 200px;
    height: 200px;
    overflow: hidden;
    border-radius: 100%;
    box-shadow: 3px 3px 8px 1px rgba(0, 0, 0, 0.3); }
    .sidebar__photo__img {
      height: 100%; }
  .sidebar__heading {
    font-family: "Roboto Slab", serif; }
  .sidebar__menu__item a {
    color: black;
    text-decoration: none; }
  .sidebar__menu__item a:hover {
    font-weight: 600; }
  .sidebar__links a {
    padding: 6px;
    text-decoration: none; }

.main {
  background-image: url("../assets/current/background.jpg");
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover; }
  .main .section {
    padding: 12px 24px; }
    .main .section:first-child {
      padding-top: 24px; }
    .main .section:last-child {
      padding-bottom: 24px; }
    .main .section p {
      font-size: 16px;
      margin: 0; }
      .main .section p:not(:last-child) {
        margin-bottom: 16px; }
    .main .section ul {
      margin: 0; }
    .main .section--header {
      color: #422C0A;
      text-transform: uppercase;
      font-size: 24px;
      font-weight: bold;
      letter-spacing: 3px;
      padding-left: 12px;
      padding-bottom: 6px; }
    .main .section--body {
      background-color: rgba(255, 255, 255, 0.6);
      padding: 24px;
      border-radius: 5px; }

.project__item:not(:last-child) {
  padding-bottom: 24px; }
.project__item__title {
  font-size: 20px;
  font-weight: bold; }
.project__item__skills {
  font-style: italic; }
</style>