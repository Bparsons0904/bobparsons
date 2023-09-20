<script>
	import WorkCard from '../../components/work-card.svelte';

	const importsResults = [
		'Import time drastically reduced from 2.5 hours to just 1 minute.',
		'Client setup time shortened from 4 weeks to 2-3 days.',
		'Implementation of a more scalable and efficient architecture for future client additions.'
	];

	const importsSolution = [
		{
			title: 'Deep Investigation',
			description:
				'Conducted a thorough review of the pre-existing imports, quickly identifying a high degree of duplicated work due to each client necessitating its unique import.'
		},
		{
			title: 'New Structure Ideation',
			description:
				'Developed a refined structure to minimize redundancy. Pivoted to a design where the majority of the import system was reusable, requiring just client-specific mappings.'
		},
		{
			title: 'Technical Advancements with Go Lang',
			description:
				'Leveraged the capabilities of Go Lang for its parallel processing, ensuring multiple routines ran concurrently. Transitioned to batching inserts, significantly amplifying efficiency.'
		},
		{
			title: 'Data Management Challenge',
			description:
				'Grappled with incoming data that spread across 100+ tables. Each client introduced distinct data, necessitating conversion into a standardized format while retaining its inherent value.'
		},
		{
			title: 'Layered Innovation',
			description:
				'Our groundbreaking approach segmented the import into layers for heightened reusability. This methodological step ushered us closer to a nearly codeless import.'
		},
		{
			title: 'Blend of Strategy & Tech',
			description:
				"The combination of strategic redesign and technological advancements didn't just solve a problem – it showcased the potential of what's achievable when both domains intersect."
		}
	];

	const communicationResults = [
		'Boosted productivity of sales reps by streamlining communication processes.',
		'Increased engagement and conversion rates with potential clients.',
		"Enhanced the CRM/'s value proposition by making it a comprehensive communication tool."
	];

	const communicationSolution = [
		{
			title: 'Unified Communication Hub',
			description:
				'Successfully integrated a feature enabling users to send, receive, and manage emails, texts, and calls directly from the CRM. This eliminated the need for third-party apps or switching between platforms.'
		},
		{
			title: 'Multimedia Support',
			description:
				'Introduced the capability to send and receive attachments, including images and videos, via texts and emails. This enriched the communication and allowed for more detailed exchanges.'
		},
		{
			title: 'Call Recording & Archival',
			description:
				'Brought in an advanced call recording feature. Sales reps could now access recorded audio for future references, aiding in training and improving sales strategies.'
		},
		{
			title: 'Holistic Communication Experience',
			description:
				'Beyond mere feature additions, we transformed the CRM into a holistic communication tool, enhancing user experience and increasing daily user engagement.'
		}
	];
</script>

<section class="opener">
	<h1>Software Development Experts</h1>
	<p>
		We enjoy the challenge of solving problems. It's what we love to do. Here is a collection of
		problems we have solved for others.
	</p>
</section>

<section class="results">
	<WorkCard
		image="/images/imports.svg"
		alt="placeholder"
		title="Slow Imports"
		problem="A scaling CRM's development team faced significant delays with their client import process. It took them nearly 4 weeks to set up a single import for each client. Once initiated, this import process consumed an average of 2.5 hours to complete for each community. Given their growth plan of adding 500 communities in the upcoming year, the existing procedure was infeasible."
		results={importsResults}
		solutions={importsSolution}
	/>
	<WorkCard
		image="images/communications.svg"
		alt="In-app Communications"
		title="In-App Communication Integration"
		problem="The client expressed the need for an integrated communication system within their CRM. Their goal extended beyond just communication; they envisaged the capacity to send/receive emails, texts, and conduct calls—all without leaving the platform."
		results={communicationResults}
		solutions={communicationSolution}
	/>
</section>

<style lang="scss">
	.opener {
		color: var(--color-text-light);
		background-color: var(--color-secondary-dark);
		padding: 2rem;
		text-align: center;
	}

	.results {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 3rem;
		padding: 2rem;
	}
</style>
