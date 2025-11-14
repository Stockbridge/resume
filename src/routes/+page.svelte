<script lang="ts">
	import Header from '$lib/Header.svelte';
	import Education from '$lib/Education.svelte';
	import Skills from '$lib/Skills.svelte';
	import Projects from '$lib/Projects.svelte';
	import Employment from '$lib/Employment.svelte';

	const header = {
		firstName: 'Chris',
		lastName: 'Stockbridge',
		email: 'chris.d.stockbridge@gmail.com',
		phone: '312.852.2533'
	};

	const education = [
		{
			degree: 'BA: Interactive Arts & Media',
			school: 'Columbia College Chicago',
			dates: 'Sep 2007 - May 2011',
			description: 'Focus: UI/UX, Web, Human Computer Interaction'
		}
	];

	const skills = [
		{
			title: 'Core Technologies',
			items: [
				'TypeScript/JavaScript',
				'HTML5/Semantic Markup',
				'CSS3/Modern CSS',
				'Node.js',
				'React',
				'Next.js'
			]
		},
		{
			title: 'Frameworks & Tools',
			items: [
				'Tailwind/CSS-in-JS',
				'Storybook/Pattern Libraries',
				'Jest/Mocha/Cypress',
				'Webpack/Vite',
				'Claude/Amazon Q',
				'Docker/ECS'
			]
		},
		{
			title: 'Specializations',
			items: [
				'Design Systems',
				'Accessibility (a11y)',
				'Performance Optimization',
				'Responsive Design',
				'SEO Best Practices',
				'Automated Delivery'
			]
		},
		{
			title: 'Architecture & Methods',
			items: [
				'Modular Components',
				'Clear API Boundaries',
				'Quality and Standards',
				'Cloud Services (AWS)',
				'Experimentation',
				'CI/CD Test and Delivery'
			]
		}
	];

	const projects = [
		{
			title: 'IMDb Pattern Library',
			dates: 'Feb 2017 - Present',
			context: 'IMDb Project',
			bullets: [
				'Work with a team to define visual patterns and support code reuse and consolidation.'
			]
		},
		{
			title: 'Celtra Deprication',
			dates: 'Aug 2016 - Oct 2016',
			context: 'IMDb Project',
			bullets: [
				'Built a module to manage and deliver date checked assets for several ad types across the IMDb site and mobile application.'
			]
		},
		{
			title: 'GIG2.0',
			dates: 'Nov 2015 - Jan 2016',
			context: 'Groupon Project',
			bullets: [
				"Worked with a team to define and support a redesign of the pattern library and core set of styles used across all of Groupon's consumer facing verticals."
			]
		},
		{
			title: 'Tiered Search',
			dates: 'Aug 2014 - Oct 2014',
			context: 'Grainger Project',
			bullets: [
				"Built, maintained and prototyped the front end for Grainger's cross category general search page functionality."
			]
		},
		{
			title: 'Typeahead Search',
			dates: 'May 2014 - Aug 2014',
			context: 'Grainger Project',
			bullets: [
				"Built, maintained and versioned the front end for Grainger's main search bar and the typeaheads interior functionality."
			]
		},
		{
			title: 'Grainger Visual Update',
			dates: 'May 2014 - Sep 2014',
			context: 'Grainger Project',
			bullets: [
				"Assisted in the Conversion of the Grainger Visual Upgrade. Distilled and consolidated design patterns across Grainger's browse path."
			]
		}
	];

	const employment = [
		{
			company: 'IMDb (Amazon Subsidiary)',
			dates: 'June 2016 - Present',
			title: 'Sr. Front End Engineer / Design Technologist',
			location: 'Seattle, WA',
			skills: [
				'TypeScript',
				'Next.js',
				'React',
				'Node.js',
				'Modern Frontend Architecture',
				'Pattern Libraries (MUI, Atomic Design)',
				'Responsive Development',
				'Modern CSS (Grid, Flex, Container Queries)',
				'Semantic HTML5',
				'Accessibility',
				'CSS-in-JS',
				'Tailwind',
				'Storybook',
				'Unit Testing (Jest, Mocha)',
				'Integration Testing (Cypress, Puppeteer, Cucumber)',
				'Build Tools (Webpack, Vite)',
				'SEO Optimization',
				'Performance Optimization',
				'Cloud Services (AWS Lambda, Fargate)',
				'GraphQL',
				'Docker',
				'CI/CD',
				'Mentoring',
				'Technical Leadership',
				'Ruby',
				'Java',
				'Python'
			]
		},
		{
			company: 'Groupon',
			dates: 'Apr 2015 - June 2016',
			title: 'UX Engineer',
			location: 'Seattle, WA',
			skills: [
				'CSS3 (Sass, Stylus)',
				'HTML5',
				'JavaScript',
				'CoffeeScript',
				'Pattern Library',
				'Unit Testing (Mocha, Jasmine)',
				'Responsive Development',
				'Semantic Markup',
				'Accessibility',
				'Git',
				'Agile',
				'Node Build Tooling (Gulp, Webpack)',
				'Template Generation (Handlebars, Hogan)',
				'Atomic Design',
				'Integration Testing',
				'SPAs'
			]
		},
		{
			company: 'Grainger',
			dates: 'Apr 2014 - April 2015',
			title: 'Front End Developer',
			location: 'Chicago, IL',
			skills: [
				'CSS3 (Less, Sass)',
				'HTML5',
				'JavaScript',
				'Semantic Markup',
				'Accessibility',
				'Git',
				'Agile',
				'Handlebars',
				'Prototyping',
				'Build Tooling (Gulp/Grunt)',
				'State management',
				'Unit Testing',
				'CI/CD Pipeline',
				'Prototyping'
			]
		},
		{
			company: 'Kaplan Inc.',
			dates: 'Sep 2013 - Apr 2014',
			title: 'UX Developer',
			location: 'Chicago, IL',
			skills: [
				'CSS3 (Stylus, Sass)',
				'HTML5',
				'Ember.js',
				'JavaScript',
				'Responsive Development',
				'Git',
				'Agile',
				'Handlebars',
				'SMACSS',
				'Node',
				'SPA',
				'Prototyping'
			]
		},
		{
			company: 'Sears Holdings',
			dates: 'Apr 2013 - Aug 2013',
			title: 'UX Developer',
			location: 'Chicago, IL',
			skills: ['CSS3', 'HTML5', 'jQuery', 'JavaScript', 'Responsive Development', 'Prototyping']
		},
		{
			company: 'Perdoceo Education Corporation',
			dates: 'Jun 2012 - May 2013',
			title: 'UI/UX Developer',
			location: 'Schaumburg, IL',
			skills: ['CSS3', 'HTML5', 'jQuery', 'JavaScript', 'Responsive Development', 'Prototyping']
		},
		{
			company: 'AlphaMetrix, LLC',
			dates: 'Jan 2009 - May 2012',
			title: 'Graphic Designer',
			location: 'Chicago, IL',
			skills: ['CSS3', 'HTML5', 'jQuery', 'ASP.net', 'Email development']
		}
	];
</script>

<main class="mx-auto max-w-210">
	<Header {...header} />
	<div class="pr-2 pl-6">
		<Skills {skills} />

		<div class="flex flex-col gap-6 sm:flex-row">
			<div class="flex-1 sm:w-1/2">
				<Employment {employment} />
			</div>
			<div class="flex-1 sm:w-1/2">
				<Education {education} />
				<Projects {projects} />
			</div>
		</div>
	</div>
</main>
