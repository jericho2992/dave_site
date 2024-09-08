<script>
	import JobCard from "./JobCard.svelte";
</script>
<main>
    <div class="top">
       <a href="../"><h1> Dave Ingersoll</h1></a>
    </div>    
    <div class="content">  
        <div class="jobs">      
            <JobCard 
                title={"Music Teacher and Assistant Marching Band Director"}
                employer = {"Weehawken BOE"}
                bullets = {[
                    {
                        text: "Managed visual, technical, and creative staff to achieve weekly goals within the seasonal project framework.",
                        skills: ["Project Managment", "Strategic Planning", "Operational Analysis"]
                    },
                    {
                        text: "Managed goals, needs, and expectations for key stakeholders to the music program such as supervisors, parents, and students",
                        skills: ["Stakeholder Management", "Outreach", "Marketing"]
                    },
                    {
                        text: "Planned concert logistics and managed inventory repairs and acquisitions central to the operations of an effective program",
                        skills: ["Project managment"]
                    }
                ]}
                ></JobCard>
            <JobCard
                title = {"Esports Coach"}
                employer = {"Concord Education"}
                bullets = {[
                    {
                        text: "Coordinated with internal and external stakeholders on goals, processes, scheduling, and pedagogy",
                        skills: ["Operations Analyis","Stakeholder Management","Customer Support"]
                    },
                    {
                        text: "Engineered a server-hosted bot to arrange matches, track team records, and create standings based on a proprietary ELO system",
                        skills: ["Node.js","Javascript","C#","Discord"]
                    },
                    {
                        text: "Engineered a live-updating overlay scoreboard to generate interactive and immersive graphics from game data during esports broadcasts",
                        skills: ["Open Broadcaster Software","HTML","CSS","Javascript","Svelte"]
                    },
                ]}
                >
            </JobCard>
            <JobCard
                title = {"Rental Services Coordinator"}
                employer = {"Boosey & Hawkes"}
                bullets = {[
                {
                        text: "Coordinated requests, contracts, materials, and rights all western-hemisphere small-rights performances for all internal and administered IP",
                        skills: ["Customer Support", ]
                    },
                    {
                        text: "Analyzed rental trends and created dashboards for collaborative strategy meetings",
                        skills: ["Operational Analysis","R","RStudio","Flexdash"]
                    },
                    {
                        text: "Engineered pricing schedule web tool that increased quoting efficiency by 78%",
                        skills: ["HTML","CSS","Javascript","Svelte"]
                    },
                ]}
                >
            </JobCard>
        </div>
        <div class="skills">
            <h2>Skills</h2>
            <div class="columns">
                <div class="left-col">
                    <h4>Coding</h4>
                    <ul>
                        <li>HTML</li>
                        <li>CSS</li>
                        <li>Javascript</li>
                        <li>Node.js</li>
                        <li>C#</li>
                        <li>R</li>
                        <li>SQL</li>
                        <li>Java</li>
                        <li>Svelte</li>
                    </ul>
                    <h4>Strategy</h4>
                    <ul>
                        <li>Marketing Analytics</li>
                        <li>Marketing Strategy</li>
                        <li>Managerial Economics</li>
                        <li>Regression Analysis</li>
                        <li>Operational Analysis</li>
                        <li>Decision Analysis</li>
                        <li>Simulation</li>
                        <li>Negotiation</li>
                        <li>Financial Analysis</li>
                        <li>Managerial Accounting</li>
                    </ul>
                </div>
                <div class="right-col">
                    <h4>Data Visualization</h4>
                    <ul>
                        <li>Tableau</li>
                        <li>RStudio</li>
                        <li>Excel</li>
                    </ul>
                    <h4>Relationship Management</h4>
                    <ul>
                        <li>Customer Support</li>
                        <li>Customer Outreach</li>
                        <li>Stakeholder Management</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</main>
<style>
    body {
        margin: 0;
        padding: 0;
        background-image: radial-gradient(rgb(0,30,30),rgb(0,50,50));
    }
    div {
        margin: 0;
        padding: 0;
    }
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		color: white;
		margin:0;
		padding:0;
		background-image: radial-gradient(rgb(0,30,30),rgb(0,50,50));
		min-height: 100vh;
		min-width: 100vw;
        font-size: 1em;
	}
    .top{
        display: flex;
        flex-direction: column;
        align-items: center;
        color: black;
    }
    .top a {
        text-decoration: none; 
        color: white;
    }
    .top a:hover {
        color: rgb(0,100,75)
    }
       @media only screen and (min-width: 601px)
    {
        .content {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-items: space-between;        
        }
        .jobs{
            display: flex;
            flex-direction: column;
            align-items: start;
            color: white; 
            min-width: 55vw;
            width: 55vw;
            max-width: 55vw;
        }
        .skills {
            display: flex;
            flex-direction: column;
            flex-wrap: nowrap;
            min-width: 30vw;
            width: 30vw;
            max-width: 30vw;
            min-height: 80vh;
            background-image: radial-gradient(rgb(0,60,60), transparent);
            margin-top: 2em;
        }
    }
    @media only screen and (max-width: 600px) 
    {
        .content {
        display: column;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-items: space-between;
        }
        .jobs{
            display: flex;
            flex-direction: column;
            align-items: start;
            color: white; 
            min-width: 80vw;
            width: 80vw;
            max-width: 80vw;
        }
        .skills {
            display: flex;
            flex-direction: column;
            flex-wrap: nowrap;
            min-width: 80vw;
            width: 80vw;
            max-width: 80vw;
            min-height: 80vh;
            background-image: radial-gradient(rgb(0,60,60), transparent);
            margin-top: 2em;
        }

    }

    .skills h2 {
        text-align: center;
    }
    .columns {
        display:flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: space-around;
    }
    .columns li {
        margin-top: 0.25em;
    }
</style>