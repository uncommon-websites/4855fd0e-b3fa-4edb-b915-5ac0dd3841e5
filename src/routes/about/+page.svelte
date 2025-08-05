<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "AI-first mindset",
			description: "Building the world's most sophisticated talent prediction models that understand what makes engineers exceptional."
		},
		{
			title: "Global remote culture",
			description: "Connecting top talent with elite opportunities regardless of location, because great minds shouldn't be limited by geography."
		},
		{
			title: "Relentless efficiency",
			description: "Eliminating the broken job hunt process by making one application reach thousands of companies instantly."
		}
	];
</script>

<SecondaryHero
	title="Skip the grind. Land the role."
	subtitle="Elite AI jobs without endless applications"
	imageSrc="/generated/image-a-group-of-young-diverse-entrepreneurs-c.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Thousands of AI engineers were facing the same brutal problem: spending months applying to hundreds of companies just to get ignored. Even for the most skilled, the job hunt meant cold emails, endless rejection, and precious time wasted not building or solving—but waiting. The system was broken. Amazing talent was being buried in inboxes. That frustration is what sparked Mercor: a better way for engineers to reach the companies they deserve.",
		"Built by two 21-year-olds who understood the inefficiencies firsthand, Mercor created a new pipeline entirely: a single application that reaches thousands of startups, powered by proprietary AI talent prediction models. Their matching system didn't just speed things up—it completely redefined the process. Backed by $100 million in funding and a $2 billion valuation, Mercor's AI conducts interviews, filters by skill and experience, and gets engineers in front of companies that are hiring right now. Fast, fair, and built for impact.",
		"Today, Mercor is the bridge between world-class AI talent and the most ambitious companies on the planet. Candidates placed through Mercor see 60% salary increases on average, with $50 million already paid out to top engineers around the globe. Hundreds of hours saved. Thousands of elite roles opened. It's not just about getting hired—it's about finding work that's worth your time."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- Team and Investors sections removed - no specific information available -->

<!-- CTA Section -->
<CallToAction
	title="Ready to level up your career?"
	subtitle="Join elite AI engineers earning 60% more"
	description="Skip the endless applications and rejections. One application reaches thousands of top companies hiring AI engineers right now. From algorithm design to frontier AI development—find roles worthy of your expertise."
	imageSrc="/generated/image-a-professional-young-engineer-working-co.webp"
	callsToAction={[
		{
			href: "/",
			label: "Apply now",
			variant: "primary"
		},
		{
			href: "/",
			label: "View opportunities",
			variant: "secondary"
		}
	]}
/>
