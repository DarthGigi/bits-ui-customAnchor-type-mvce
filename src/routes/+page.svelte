<script lang="ts">
	import { Tooltip } from 'bits-ui';

	let asteriskRef = $state<HTMLElement | null>(null);
</script>

<Tooltip.Provider>
	<Tooltip.Root>
		<Tooltip.Trigger>Hello <span bind:this={asteriskRef}>*</span></Tooltip.Trigger>
		<Tooltip.Portal>
			<Tooltip.Content customAnchor={asteriskRef}>
				World
				<Tooltip.Arrow />
			</Tooltip.Content>
		</Tooltip.Portal>
	</Tooltip.Root>
</Tooltip.Provider>
