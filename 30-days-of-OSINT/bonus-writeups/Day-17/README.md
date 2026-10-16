# Ghost of OSINT Station — Day 17: Voice Mail

Repo folder for Day 17 of the Ghost of OSINT Station case.

## Contents

- **`day17.md`** — the full writeup
- **`media/`** — source images used in this challenge:
  - `day_17.jpg` — the challenge image (the answering machine, LCD reading "NEW MESSAGE: 1, voice_mail.mp3").
  - `morse_loop.png` — waveform screenshot decoding to the Morse word "LOOP."
  - `morse_never.png` — waveform screenshot decoding to the Morse word "NEVER."
  - `morse_ends.png` — waveform screenshot decoding to the Morse word "ENDS."

## Summary

Three static waveform screenshots encoded short Morse words via pixel-width timing rather than audio. Measuring dot/dash widths directly on the images (not listening to a recording) produced "LOOP," "NEVER," "ENDS." The words came fast; the flag didn't, over a single dropped character in the format string during copy-paste. Full account in the Markdown.

## Case context

Part of the larger Ghost of OSINT Station case (Dr. Julian Vance). See the main case repo for the full Day 11–20 writeup and case analysis.
