# Hold Me Closer, Tony Danza 

## Luis Montes
### Iced Dev, Phoenix, AZ 
- [Speaker's Notes (Placeholder)]()
- [Post-conference YouTube Recording (Placeholder)]()
## Abstract: 
Mixing AI and karaoke together for great justice.
## Community talk notes:
Brief history introducing CD+G format.
Creating a pipeline by taking a music file to pass it through Demus for Stems, Whisper for lyrics

Storing lyrics - embed the data as an atom into .stem.mp4
[open source karaoke software](https://github.com/monteslu/loukai)

### A brief history
First song played: 1877. Karaoke: 1980s. **CD+G** (CD + graphics) is backward compatible — and rough: 2.27% graphics to 97.73% audio, ~26.5 kbit/s for video, 288×192 at 16 of 4096 colors, 6×12 tiles. KJs have deep CD+G catalogs. We could probably do better… and we can render CD+G in canvas with WebGL.

### The DJ's dream: stems
Mix two songs together by separating the music out — drums for beat matching, vocals for mashups and remixes. Stems used to be expensive to get.
- **AI source separation** — as of 2024, DJ software includes it.
- **[Demucs](https://github.com/adefossez/demucs)** — MIT license, good quality, PyTorch; breaks audio out into files. Is **MP4 stems** the new standard? (MP4 isn't a movie file — it's just a container.)
- The result is *real original audio*, not a MIDI recreation — so you can control vocal volume, or mute it entirely.

### Lyrics
- **[Whisper](https://github.com/openai/whisper)** (OpenAI) — feed it the isolated vocals from Demucs to get transcription *and* timing, then put it in the MP4 file. Whisper isn't perfect — timing can be slightly off, and it struggles with some lyrics.
- **LLMs for lyrics** — fix the transcription errors while keeping the timing right; you can also pass along open-source lyrics. (Hence "Hold me closer, Tony Danza" 🤣.)
- Corrected lyrics still want a file: the MP4 spec uses **atoms** — standard atoms, a stem atom, and a kara atom for synced karaoke lyrics.

### Putting it together
A pipeline — plus an open-source player. Other pieces:
- **CREPE** — musical key detection.
- **Butterchurn** — the WinAMP visualizer stuff, encoded in WebGL.

**Karaoke in 2026:** `.stem.mp4` is a worthy successor to CD+G. (See also: youmaynotneedelectron.com.)
