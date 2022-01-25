<script>
	import NoteInput from './NoteInput.svelte'
	let name = 'world';
	let octave= 0
	let letter= 'C'
	let alter= 0
	let musicalAlphabet=  ['C','D','E','F','G','A','B']
</script>

<NoteInput>
		<legend slot="legend" class="input-legend">
			Note 1
		</legend>
	
		<input type=number bind:value={octave} min=0 name="octave" slot="octave" class="input-field"/>
	
		<select bind:value={letter} slot="letter" class="input-field">
			{#each musicalAlphabet as noteLetter}
				<option value={noteLetter}>
					{noteLetter}
				</option>
			{/each}			
		</select>
	
		<input type=number bind:value={alter} name="alter" slot="alter" class="input-field"/>
</NoteInput>

<style>
	.input-field {
		margin: 0.5em 0;
		border-radius: 2em;
		text-align: center;
		border-color: black;
	}
	.input-legend {
		text-align: center;
		font-weight: bold;
		font-size: 1.5em;
		font-family: Arial;
	}
</style>