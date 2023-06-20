# yolk-demo

earthsea-like demo, configurable scales/tuning, pattern recording & pattern banks, no stuck notes. usues [`crops`](https://github.com/andr-ew/crops), [`pattern_time_extended`](https://github.com/andr-ew/pattern_time_extended), [`produce`](https://github.com/andr-ew/produce), [`tune`](https://github.com/andr-ew/tune), and [`arqueggiator`](https://github.com/andr-ew/arqueggiator)

## norns

- **K1 (hold):** edit tuning
  - **E1:** scale
  - **E2:** tuning system (12tet, arabic maquam, or just intonnation variants)
  - **E3:** row tuning
  - **K2 - K3:** fret marks
 
## grid

### mode: poly & mono

in the first two modes, grid is an earthsea-like grid keyboard, polyphonic or monophonic.

![diagram of the grid interface. text description forthcoming](/lib/doc/grid_poly_mono.png)

**keymap:** grid keyboard. edit the tuning by holding K1.

**scroll columns:** transpose up or down one degree within the current scale. this shifts your view of the keyboard left or right.

**scroll rows:** transpose up or down based on the **row tuning** interval. this shifts your view of the keyboard up or down.

**pattern slots:** 9 slots for recording input sequences on the keymap. use them like this:

- **single tap**
  - (blank pattern): begin recording
  - (recording pattern): end recording, begin looping
  - (playing pattern): play/pause playback. only one slot is active at a time
- **double tap:** overdub pattern
- **hold:** clear pattern

**pattern reverse & rate:** set the direction & playback rate of the current pattern.

### mode: arqueggiator

the arqueggiator is a mix between an arpeggiator & a sequencer.

![diagram of the grid interface. text description forthcoming](/lib/doc/grid_arq.png)

**keymap:** there are a few ways to interact with the arqueggiator:

- **hold & release multiple keys:** creates a new arq (clears any previous keys). notes are played in the order they are pressed, including double-presses on the same key.
- **single tap**
   - (blank key): insert a note at the current point in the arquence
   - (active key): mute gate at note
- **double tap:** add repeat to note
- **hold single key:**
   - (repeated key): remove repeat
   - (active key): remove note

**snapshots:** 6 snapshots to store & recall arquences. use them like this:

- **double tap:** write to slot
- **single tap** read from slot
- **hold:** clear slot

**pattern slots:** you can record changes made to the arqueggiator as well, including recalled snapshots.

**arq reverse & rate:** set the direction of arq playback and the clock multiple/division.

### K1 (hold): edit tuning

![diagram of the grid interface. text description forthcoming](/lib/doc/grid_scale.png)
