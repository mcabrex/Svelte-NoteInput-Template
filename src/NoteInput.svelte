<script>
</script>

<fieldset class="note-inputs">
   <slot name="legend">
      <legend>Note Inputs</legend>
   </slot>
	
   <label for="octave" class="input-title">
      Octave
   </label>
   <slot name="octave" class="input-octave"></slot>

   <label for="letter" class="input-title">
      Letter
   </label>
   <slot name="letter"></slot>
	
   <label for="alter" class="input-title">
      Alter
   </label>
   <slot name="alter"></slot>
</fieldset>

<style>
  .note-inputs {
		 width: fit-content;
		 margin: 0.5em;
		 padding: 1em;
		 grid-template-columns: [label] 30% [input] 70%;
		 grid-template-rows: [octave] 33% [letter] 33% [alter] 33%;
		 display: grid;
  }
	.input-title {
		align-self: center;
		margin: 0.5em 0;
	}
</style>