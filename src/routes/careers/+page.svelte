<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Flexible Work",
			description: "Remote-first with flexible hours that respect work-life balance.",
			icon: IconBriefcase
		},
		{
			title: "Growth Opportunities",
			description: "Continuous learning with mentorship and education stipends.",
			icon: IconUsers
		},
		{
			title: "Comprehensive Benefits",
			description: "Health coverage, retirement plans, and generous paid time off.",
			icon: IconHeart
		}
	];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Gabriela Torres",
    position: "Software Engineer",
    company: "Engineering Team",
    quote: "XBOW stands out for its supportive, genuinely inclusive environment. I’m encouraged to bring new ideas and collaborate cross-functionally every day. The mentorship here is real—people care about your growth and success.",
    image: "/generated/image-a-professional-latina-female-engineer-wo.webp"
  },
  {
    name: "Darius Moore",
    position: "Head of Product",
    company: "Product Team",
    quote: "I’ve led teams across tech, but at XBOW, it’s different—the sense of purpose, transparency, and trust is unmatched. You’re trusted with big challenges and given the room to drive real impact, knowing leadership has your back.",
    image: "/generated/image-a-black-male-senior-product-leader-in-a-.webp"
  },
  {
    name: "Jamie Liu",
    position: "Operations Associate",
    company: "Operations",
    quote: "Coming in as a recent grad, I was looking for a place where I could learn and be supported. XBOW made me feel welcome from day one, and I’m empowered to make meaningful contributions regardless of my role or how I identify.",
    image: "/generated/image-a-young-asian-non-binary-operations-empl.webp"
  }
];

	const processSteps = [
		{
			step: 1,
			title: "Apply",
			description:
				"Submit your application through our careers portal with your resume and portfolio."
		},
		{
			step: 2,
			title: "Interview",
			description: "Meet with our team to discuss your experience, skills, and career aspirations."
		},
		{
			step: 3,
			title: "Welcome aboard",
			description: "Join our team and start your journey building the future with us."
		}
	];

	const values = [
		{
			icon: IconHeart,
			title: "Passion",
			description: "We're driven by a shared passion for innovation and excellence."
		},
		{
			icon: IconUsers,
			title: "Collaboration",
			description: "We believe in teamwork and collaboration to achieve great things."
		},
		{
			icon: IconGlobe,
			title: "Global Impact",
			description: "We're committed to making a positive impact on the world."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
    title="Advance autonomous security with top minds"
    subtitle="Grow fast. Build boldly. Secure the web together."
    imageSrc="/generated/image-a-diverse-team-of-professionals-collabor.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Push boundaries, shape the future, build with impact." />

<div class="prose prose-primary mx-auto max-w-3xl mb-12">
  <ul>
    <li><strong>Technology with edge.</strong> Work on agentic AI and deep offensive security problems not tackled anywhere else.</li>
    <li><strong>Impact from day one.</strong> Your work protects real users, improves live deployments, and advances the state of the art.</li>
    <li><strong>Learn from elite minds.</strong> Join a stacked team spanning competitive hacking, compiler infrastructure, machine learning, and startups.</li>
    <li><strong>Own value, not fluff.</strong> Fast cycle times. Real customers. Close ownership over what you ship.</li>
  </ul>
</div>
<section class="grid md:grid-cols-3 gap-4">
  <Card title="Flexible work" description="Remote-first with flexible hours and a focus on trust and autonomy." icon={IconBriefcase} />
  <Card title="Growth & learning" description="Advance your skills with mentorship, education stipends, and unique peer learning opportunities." icon={IconUsers} />
  <Card title="Comprehensive benefits" description="Competitive pay, ownership opportunities, health coverage, and generous time off." icon={IconHeart} />
</section>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
