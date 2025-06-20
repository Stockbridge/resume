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
      degree: 'Bachelor of Arts (B.A.), Interactive Arts and Media',
      school: 'Columbia College Chicago',
      dates: '2007 – 2011',
      description: 'I studied Interactive Media with a focus on the presentation layer of complex applications and interactive prototyping. Web Technologies'
    }
  ];

  const skills = [
    ['Svelte, TypeScript, JavaScript, React', 'Node.js, Express, REST APIs'],
    ['CI/CD, Docker, AWS', 'Agile, TDD, Mentorship']
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
        'Worked with a team to define and support a redesign of the pattern library and core set of styles used across all of Groupon\'s consumer facing verticals.'
      ]
    },
    {
      title: 'Tiered Search',
      dates: 'Aug 2014 - Oct 2014',
      context: 'Grainger Project',
      bullets: [
        'Built, maintained and prototyped the front end for Grainger\'s cross category general search page functionality.'
      ]
    },
    {
      title: 'Typeahead Search',
      dates: 'May 2014 - Aug 2014',
      context: 'Grainger Project',
      bullets: [
        'Built, maintained and versioned the front end for Grainger\'s main search bar and the typeaheads interior functionality.'
      ]
    },
    {
      title: 'Grainger Visual Update',
      dates: 'May 2014 - Sep 2014',
      context: 'Grainger Project',
      bullets: [
        'Assisted in the Conversion of the Grainger Visual Upgrade. Distilled and consolidated design patterns across Grainger\'s browse path.'
      ]
    }
  ];

  const employment = [
    {
      company: 'IMDb.com',
      dates: 'Jun 2016 - Present',
      title: 'Sr Front End Engineer',
      location: 'Seattle, WA',
      description: 'Agile methodologies, TypeScript, JavaScript, React, jQuery, CSS, CSS3, Styled Components, HTML5, Semantic Markup, Pattern Library Creation and Management, Webpack, Grunt, Automated Build Processes, Graceful Degradation, Progressive Enhancement, Git, Jest, Cypress, Mocha, Chai, Cucumber, Performance and Latency Auditing',
      skills: 'TypeScript · Testing · React.js · W3C Accessibility · CI/CD · HTML5 · CSS'
    },
    {
      company: 'Groupon',
      dates: 'Apr 2015 - Jun 2016',
      title: 'UX Developer II',
      location: 'Seattle, WA',
      description: 'Agile Methodologies, JavaScript, CSS3, HTML5, Gulp, Chrome Extensions, Prototype Generation, Stylus, Git, Semantic Markup, Interaction Layer Development, jQuery, Unit Testing, Integration Testing, Styles as a Service, Mocha, Internationalization, Localization',
      skills: 'Communication · Debugging · Computer Science · Web Technologies'
    },
    {
      company: 'Grainger',
      dates: 'Apr 2014 - Apr 2015',
      title: 'Front End Developer',
      location: 'Chicago, IL',
      description: 'Scrum Methodology, LESS, Handlebars, CSS3, HTML5, jQuery, JavaScript, Grunt, Gulp, Prototype Generation, Stylus, Git, Semantic Markup, Search Functionality, Graceful Degradation, Localization',
      skills: 'Communication · Debugging · Computer Science · Web Technologies'
    },
    {
      company: 'Kaplan University / Qualified',
      dates: 'Aug 2013 - Apr 2014',
      title: 'UX Developer',
      location: 'Chicago, IL',
      description: 'My time at Kaplan University was spent on the Qualified project. Scrum Methodology, Stylus, SASS, CSS3, HTML5, ember.js, node.js, JavaScript, jQuery, Prototype Generation, Web Applications Development, Presentation Layer Development, Semantic Markup, Git, Documentation',
      skills: 'Communication · Debugging · Computer Science · Web Technologies'
    },
    {
      company: 'Sears Holdings Corporation',
      dates: 'Apr 2013 - Jul 2013',
      title: 'UX Developer',
      location: 'Chicago, IL',
      description: 'I spent my time at Sears Holdings working on the ShopSears, GameOn, and IRLabs projects. CSS3, HTML5, JavaScript, JQuery, Responsive Development, Prototype Generation, Prototype Design, Design Patterns, UI/UX Development, Object Oriented Programming, Git, SVN, Documentation, PHP, Wordpress, jQuery UI, jQuery Mobile, Axure RP, Mobile Point of Sale.',
      skills: 'Communication · Debugging · Computer Science · Web Technologies'
    },
    {
      company: 'Career Education Corporation',
      dates: 'May 2012 - Apr 2013',
      title: 'UI/UX Developer',
      location: 'Schaumburg, IL',
      description: 'While I was with CEC I worked on the Conexus and Castle projects. UI/UX, CSS, HTML, JavaScript, JQuery, Web Design, Icon Design, Prototyping, Branding, User Flows, Wire Framing, Styling Microsoft Controls, Theming Telerik Controls, SafeSource, Graceful Degradation, Axure RP',
      skills: 'Communication · Debugging · Computer Science · Web Technologies'
    },
    {
      company: 'AlphaMetrix, LLC',
      dates: 'Jan 2009 - Apr 2012',
      title: 'Graphic Designer',
      location: 'Chicago, IL',
      description: 'HTML, CSS, Print/Web Design, Print/Web Layout, Designing Presentations, Slicing, Photoshop, Illustrator, Marketing Emails, Wordpress, Wordpress Themes, Content Management, eTouches, Sharepoint Event Signage, Image Generation, Theming Telerik Controls, Small Team Management',
      skills: 'Communication · Debugging · Web Technologies'
    }
  ];
</script>

<main class="mx-auto max-w-[1000px] p-[10px]">
  <Header {...header} />
  <Employment {employment} />
  <Education {education} />
  <Skills {skills} />
  <Projects {projects} />
</main>
