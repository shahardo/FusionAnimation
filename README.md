# Nucleus to Grid

An animated explainer of nuclear fusion, from two nuclei to a working power plant. It's a single self-contained HTML page with no build step: open `index.html` in a browser.

## Chapters

1. **The Coulomb barrier**: deuterium and tritium repel each other.
2. **Fusion**: three pairs at rising temperatures. The last pair tunnels through the barrier and fuses into helium-4 and a neutron. A chart shows the 0.0189 u of mass that becomes 17.6 MeV.
3. **Magnetic confinement**: a tokamak's coils, the twisted magnetic field and the plasma. Fusion flashes release neutrons that escape the field.
4. **Laser inertial confinement**: a spherical chamber where lenses focus laser beams onto a fuel pellet (direct drive), followed by repeated pellet shots.
5. **Capturing the energy**: both reactor types surround the fuel with a lithium blanket that is heated by neutrons. The blanket feeds the coolant loop and breeds tritium, which an extraction plant returns to the reactor as fuel.
6. **The power plant**: steam generator, turbine, generator, condenser with its cooling-water loop, cooling tower and grid.

## Controls

- Play/pause and restart buttons, a scrubber, and chapter buttons.
- Keyboard: Space plays and pauses; the left and right arrow keys jump between chapters.
- A timestamped narration script for a voice-over is included on the page.

## How it works

Everything is drawn on one `<canvas>`. Each frame is computed purely from the current playback time, so scrubbing and jumping between chapters are exact. Each chapter is an entry in the `CH` array with a duration, timed caption lines (`beats`) and a `draw(lt)` function. Fonts load from Google Fonts, with system fallbacks.
