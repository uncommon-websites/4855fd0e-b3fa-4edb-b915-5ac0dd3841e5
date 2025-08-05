<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
	import Hero from "$lib/components/layout/hero-sections/Hero.svelte";
</script>

<CustomerCardHero
	title="Land elite AI roles with 60% salary increases"
	subtitle="Join thousands of AI engineers and data scientists who've leveraged our AI talent prediction models to secure top-tier remote opportunities at Silicon Valley startups."
	centered={true}
	customers={[
		{
			name: "Sarah Chen",
			position: "ML Engineer at Anthropic",
			imageSrc: "/generated/image-a-professional-female-engineer-in-a-mode.webp"
		},
		{
			name: "Marcus Rodriguez",
			position: "Data Scientist at OpenAI",
			imageSrc: "/generated/image-a-professional-male-scientist-in-a-clean.webp"
		},
		{
			name: "Emily Thompson",
			position: "AI Researcher at Google",
			imageSrc: "/generated/image-a-professional-female-specialist-in-a-te.webp"
		},
		{
			name: "David Kim",
			position: "Senior Engineer at Stripe",
			imageSrc: "/generated/image-a-professional-male-researcher-in-a-mode.webp"
		},
		{
			name: "Jessica Park",
			position: "Technical Lead at Meta",
			imageSrc: "/generated/image-a-professional-female-software-engineer-.webp"
		}
	]}
/>
<LogoScroller 
	label="Trusted by industry leaders"
	logoUrls={[
		'https://cdn.brandfetch.io/openai.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/anthropic.com/w/400/h/400/logo',
		'https://cdn.brandfetch.io/huggingface.co/w/400/h/400/logo',
		'https://cdn.brandfetch.io/databricks.com/w/400/h/400/logo'
	]}
/>

<Summary
	title="How we work"
	text="Mercor connects elite AI engineers and data scientists to thousands of companies through a single application, leveraging proprietary AI talent prediction models to secure remote roles with 60% salary increases. Our AI-powered interviewing system eliminates hundreds of hours of job searching while matching top-tier technical talent with Silicon Valley startups and leading tech companies. With $50 million already paid out to talent and 5,000+ active opportunities, we're transforming how exceptional AI professionals find their next career breakthrough."
/>

<Testimonials
	testimonials={[
		{
			name: "Priya Sharma",
			position: "Senior ML Engineer",
			company: "Anthropic",
			quote:
				"Mercor's AI interviewer identified my strengths in model optimization and matched me perfectly with Anthropic. Instead of spending months applying to hundreds of companies individually, I had three offers within two weeks and increased my salary by 75%.",
			image: "/generated/image-a-professional-female-engineer-in-a-mode.webp"
		},
		{
			name: "Alex Chen",
			position: "Data Scientist",
			company: "Scale AI",
			quote:
				"The single application process saved me over 200 hours of job searching. Mercor's talent prediction model understood my deep learning expertise better than traditional recruiters and connected me with Scale AI's advanced computer vision team. My new role pays $180k more than my previous position.",
			image: "/generated/image-a-professional-male-scientist-in-a-works.webp"
		},
		{
			name: "Isabella Rodriguez",
			position: "AI Research Engineer",
			company: "OpenAI",
			quote:
				"After years of getting rejected by top-tier companies, Mercor's AI assessment highlighted my research contributions in transformer architectures. Within three weeks, I was interviewing with OpenAI's GPT team. The platform eliminated the guesswork and landed me my dream role in frontier AI development.",
			image: "/generated/image-a-professional-female-specialist-in-a-de.webp"
		}
	]}
/>

<Features
	title="Why elite AI talent chooses Mercor"
	subtitle="Our proprietary AI technology transforms how top engineers find their next opportunity"
	features={[
		{
			title: "AI talent prediction models",
			description:
				"Our proprietary AI instantly matches your skills to thousands of companies, eliminating months of manual applications and dramatically increasing your response rate."
		},
		{
			title: "Single application, infinite reach",
			description:
				"Apply once and get matched to thousands of Silicon Valley startups and tech companies. Save hundreds of hours while accessing opportunities you'd never find on your own."
		},
		{
			title: "60% salary increases guaranteed",
			description:
				"Join the thousands of AI engineers who've secured life-changing salary increases through our elite placement network focused on top 1% compensation."
		},
		{
			title: "AI-powered interviews",
			description:
				"Skip the endless screening calls with our intelligent interviewing system that conducts natural 20-minute conversations, letting your expertise shine."
		},
		{
			title: "Elite remote opportunities",
			description:
				"Access frontier AI development roles at the world's most exciting companies, from OpenAI to Anthropic, all designed for global remote work."
		},
		{
			title: "Global Silicon Valley access",
			description:
				"Break geographic barriers and compete for Silicon Valley-level opportunities regardless of your location, with our global talent network."
		}
	]}
/>
<AboutTeaser />
<CallToAction 
	title="Stop applying. Start getting hired."
	subtitle="Join 5,000+ elite AI engineers"
	description="Join thousands of engineers using Mercor to skip the job hunt and land top-tier remote roles with 60%+ salary increases. One application reaches thousands of companies—no more endless applications or ghosted emails."
	imageSrc="/generated/image-a-cheerful-and-successful-ai-engineer-is.webp"
	callsToAction={[
		{
			href: "/apply",
			label: "Apply once, get matched fast",
			variant: "primary"
		},
		{
			href: "/how-it-works",
			label: "See how it works",
			variant: "secondary"
		}
	]}
/>
