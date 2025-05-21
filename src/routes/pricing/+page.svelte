<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Luis Cervantes",
      position: "Security Engineer",
      company: "VistaData Group",
      quote:
        "We saw value from XBOW within days. It flagged real vulnerabilities our internal team missed and eliminated hours of manual testing each sprint. Worth every dollar for the time saved and peace of mind.",
      image: "/generated/image-a-latino-male-in-a-business-suit-stands-.webp"
    },
    {
      name: "Yue Lin",
      position: "Head of Application Security",
      company: "MiraeSoft",
      quote:
        "XBOW makes advanced security testing simple. We gained actionable, verified results without needing AI expertise on staff. Easily justified our investment by slashing consultant spend by half.",
      image: "/generated/image-an-east-asian-female-in-a-stylish-blouse.webp"
    },
    {
      name: "Kwame Batiste",
      position: "CTO",
      company: "Tango Ledger",
      quote:
        "XBOW integrated into our workflow seamlessly. It's fast, thorough, and the clarity of reporting let us act immediately. We increased security coverage with less effort than ever before.",
      image: "/generated/image-a-black-male-in-an-executive-suit-is-pos.webp"
    }
  ]}
/>

<CallToAction
  title="Find vulnerabilities before attackers do"
  subtitle="Agentic AI protects your web app—automatically"
  description="XBOW runs real attacks using agentic AI—just like an attacker, but safely. No scanning, scripting, or manual tuning. Just real, exploitable findings from your own app. It works: XBOW has succeeded on 75% of benchmark challenges and uncovered critical CVEs in real-world open-source apps, automatically. There’s no setup, no configuration, and no requirement for security or AI expertise. Access is limited to verified companies to ensure responsible use. See how your app holds up—before someone else does."
  imageSrc="/generated/image-a-cheerful-professional-is-interacting-w.webp"
  callsToAction={[{ href: '/book-demo', label: 'Book a demo', variant: 'primary' }]}
/>
