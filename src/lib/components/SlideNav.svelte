<script lang="ts">
	export let part: string | undefined = undefined;
	export let section: string | undefined = undefined;
	export let item: string | undefined = undefined;

	const parts = [
		{
			key: 'ownership',
			label: 'Ownership',
			slug: '3code_models',
			sections: [
				{
					key: 'code',
					label: 'Code Ownership',
					slug: '3code_models',
					items: [
						{ key: 'strict', label: 'Strict', slug: '4strict' },
						{ key: 'weak', label: 'Weak', slug: '5weak' },
						{ key: 'toyota', label: 'Toyota Way', slug: '6toyota' },
						{ key: 'collective', label: 'Collective', slug: '7collective' },
					]
				},
				{
					key: 'operational',
					label: 'Operational',
					slug: '8system',
					items: [
						{ key: 'endtoend', label: 'End-to-End', slug: '8a_end_to_end' },
						{ key: 'service', label: 'Service', slug: '8b_service' },
						{ key: 'lean', label: 'Lean', slug: '8c_lean' },
					]
				},
				{
					key: 'roles',
					label: 'Role-Based',
					slug: '9roles',
					items: []
				}
			]
		},
		{
			key: 'frameworks',
			label: 'Industry Frameworks',
			slug: '9c_frameworks',
			sections: [
				{ key: 'toc', label: 'Theory of Constraints', slug: '10toc', items: [] },
				{ key: 'conway', label: "Conway's Law", slug: '11conway', items: [] },
				{ key: 'jidoka', label: 'Jidoka', slug: '12jidoka', items: [] },
				{ key: 'toil', label: 'Toil', slug: '13toil', items: [] },
				{ key: 'dora', label: 'DORA', slug: '14dora', items: [] },
			]
		},
		{
			key: 'micro',
			label: 'Micro Ownership',
			slug: '15micro',
			sections: [
				{ key: 'overview', label: 'Micro Ownership', slug: '15micro', items: [] },
				{ key: 'mindset', label: 'Mindset', slug: '16mindset', items: [] }
			]
		}
	];

	$: activePart = parts.find((p) => p.key === part) ?? null;
	$: activeSection = activePart?.sections.find((s) => s.key === section) ?? null;
	$: activeItems = activeSection?.items ?? [];
</script>

<nav class="flex flex-col gap-2.5">
	<!-- Row 1: the three top-level parts -->
	<div class="flex items-center gap-10">
		{#each parts as p}
			<a
				href="/{p.slug}"
				class="text-sm tracking-wide transition-colors duration-150"
				class:text-yellow-400={activePart?.key === p.key}
				class:font-semibold={activePart?.key === p.key}
				class:text-gray-700={activePart?.key !== p.key}
				class:hover:text-gray-500={activePart?.key !== p.key}
			>
				{p.label}
			</a>
		{/each}
	</div>

	<!-- Row 2: sections within the active part -->
	{#if activePart}
		<div class="flex items-center gap-7">
			{#each activePart.sections as s}
				<a
					href="/{s.slug}"
					class="text-sm transition-colors duration-150"
					class:text-gray-100={activeSection?.key === s.key}
					class:underline={activeSection?.key === s.key}
					class:decoration-teal-600={activeSection?.key === s.key}
					class:underline-offset-4={activeSection?.key === s.key}
					class:text-gray-600={activeSection?.key !== s.key}
					class:hover:text-gray-400={activeSection?.key !== s.key}
				>
					{s.label}
				</a>
			{/each}
		</div>
	{/if}

	<!-- Row 3: items within the active section (optional — only when items exist) -->
	{#if activeItems.length > 0}
		<div class="flex items-center gap-7">
			{#each activeItems as it}
				<a
					href="/{it.slug}"
					class="text-sm transition-colors duration-150"
					class:text-gray-100={item === it.key}
					class:underline={item === it.key}
					class:decoration-teal-600={item === it.key}
					class:underline-offset-4={item === it.key}
					class:text-gray-600={item !== it.key}
					class:hover:text-gray-400={item !== it.key}
				>
					{it.label}
				</a>
			{/each}
		</div>
	{/if}
</nav>
