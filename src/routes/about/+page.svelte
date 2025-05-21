<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
	title="Solving world hunger"
	subtitle="one step at a time"
	imageSrc="https://source.unsplash.com/random/?people"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"We started in 2018 with a simple goal: make helpful tech that people actually need. While many chase profits, we chose to do things differently.",
		"Beyond making good products, we care about doing the right thing, being kind to our planet, and making sure everyone can use what we build. That's our compass.",
		"From day one, we've asked ourselves: 'Does this actually help people?' This question gets us through tough calls and shapes who we are. We're playing the long game here.",
		"We think about how our work affects real people's lives. We build tech that brings people together, keeps your information safe, and treats everyone fairly. When we stick to these basics, good things happen."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our team."
  subtitle="Security, AI, and engineering expertise"
  stakeholders={[
    {
      name: "Oege de Moor",
      position: "Founder & CEO",
      bio: "Previously founded Diffblue, professor of computer science at Oxford, and leader in AI-driven security research.",
      image: "/generated/image-a-professional-male-ceo-headshot-with-a-.webp"
    },
    {
      name: "Nico Waisman",
      position: "Head of Security",
      bio: "Globally recognized security researcher with experience at GitHub, Immunity, and leading offensive security teams.",
      image: "/generated/image-a-professional-male-security-researcher-.webp"
    },
    {
      name: "Albert Ziegler",
      position: "Head of AI",
      bio: "AI expert with deep learning experience across large-scale projects in academia and industry.",
      image: "/generated/ai_headshot.png"
    },
    {
      name: "Andrew Rice",
      position: "Head of Engineering",
      bio: "Engineering leader and computer science professor specializing in systems and software reliability.",
      image: "/generated/engineering_headshot.png"
    },
    {
      name: "Aqeel Siddiqui",
      position: "Head of Operations",
      bio: "Operations lead with broad expertise managing high-performing technical and research teams.",
      image: "/generated/image-a-professional-male-operations-headshot-.webp"
    }
  ]}
/>

<StakeholderGrid
	stakeholderType="investor"
	title="Backed by the best."
	subtitle="Point Nine, TSIC and others"
	stakeholders={[
		{
			name: "Point Nine Capital",
			image: "https://cdn.brandfetch.io/pointnine.com/w/400/h/400/logo?c=1id_elLz2Bd5Ej-dWo7"
		},
		{
			name: "TSIC Ventures",
			image: "https://cdn.brandfetch.io/tiny.vc/w/400/h/400/logo?c=1a2b3c4d5e"
		},
		{
			name: "Sequoia Capital",
			image: "https://cdn.brandfetch.io/sequoiacap.com/w/400/h/400/logo"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction
	title="Ready to collaborate?"
	subtitle="Let's create something amazing"
	description="Join the companies already leveraging our expertise to transform their digital presence and achieve their business goals."
/>
