# NoteInput Component Template - Svelte 📁

# Usage

A standardized fieldset for note input through Svelte. 

Currently there are only three attributes for the note that this component cares about: 

- **The Octave** An octave is the distance between one pitch and another with is double it's frequency. Every octave is divided into 12 semitones.

- **The Musical Alphabet** The Musical Alphabet "A B C D E F G" defines every note in an octave. 

- **The Alter** The Alter represents the chromatic alteration of a note in semitones (e.g., -1 for flat, 1 for sharp)

The *NoteInput* component is responsible for the composition of the fields inside it's fieldset, the labels, a default legend, and the fieldset itself. 

# Slots 🎰

The element used to fill a Svelte **slot** require at the minimum a *slot* attribute. Additionally for this particular component, any Svelte **slot** that has a <\label\> preceding it must be filled by some kind of form field with a *name* attribute corresponding to it's *slot* attribute in order to match up with it's \<label\>. 

There are 4 Svelte **slots** that NoteInput cares about: 

*Note that the child content is simply what I used to place in the **slot**, feel free to use any kind of form input that you think best suits your needs*

1. **Slot 1:** 
   - Slot name: *"legend"*
   - Child content: \<legend slot="legend">
   - Constraints: Every fieldset is required to have exactly one *legend* for accessibility reasons, therefore there is a default legend set up in case you do not put one up. 
2. **Slot 2:**
   - Slot name: *"octave"*
   - Child content: \<input type="number" slot="octave" name="octave" min=0>
   - Constraints: Octaves can only be positive so the *min* value has to be set to 0, the *max* value can be set to anything.
3. **Slot 3:**
   - Slot name: *"letter"*
   - Child content: \<select slot="letter">
   - Constraints: The letters used in this **slot** must follow the *Musical Alphabet*, I suggest starting from 'C' but any order is fine.
4. **Slot 4:**
   - Slot name: *"alter"*
   - Child content: \<input type="number" slot="alter" name="alter">
   - Constraints: The *alter* **slot** does not technically have any *min* or *max* value limit but generally speaking alters are limited to multiples of two at best *ie: double sharps or double flats*