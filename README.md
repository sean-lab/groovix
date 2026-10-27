# GROOVIX

**PLAY · LOOP · MIX.** A three-track groovebox that runs in the browser: synths and recorded
instruments, a 16-step drum machine, loop recording, a voice track that turns a hummed melody into
notes, and 26 example mixes from house and lo-fi to bossa nova, ppongjjak, samba and Pachelbel's Canon.
The screen is available in Korean, English and Japanese.

Live: <https://sanghyunpark.pages.dev/apps/groovix/>

## What's inside

- **Three tracks** (bass, chords, lead), each with its own sound, level and mute, plus a piano roll.
- **Sounds:** 12 synth patches (two oscillators, sub, noise, 24 dB filter, two envelopes, LFO,
  drive, chorus, delay and reverb) and 11 recorded instruments.
- **Beats:** six synthesized drum voices on a 16-step grid with accents and swing.
- **Voice:** upload a recording (or use the microphone where the browser allows it); it plays with
  the loop, and TO NOTES tracks its pitch (YIN) into notes on any track.
- **Files:** NEW clears everything for a song of your own, SAVE/OPEN a song file (`.json`), EXPORT a `.zip`
  with a WAV of the song and a MIDI file.

## How it's built

One `index.html` with plain HTML, CSS and JavaScript, no libraries and no build step.
Sound comes from the Web Audio API; the recorded instruments are short MP3s in `samples/`
(see [CREDITS.md](CREDITS.md)).

Run it locally from this folder (the samples are fetched, so open it over HTTP, not `file://`):

```bash
python3 -m http.server 8000
# http://localhost:8000/   add ?lang=ko or ?lang=ja for Korean or Japanese
```

## Releases

Push a `v*` tag. The Release workflow packs `index.html` and `samples/` into
`groovix-<tag>.tar.gz` and attaches it to a GitHub Release. The site
([sanghyunpark.dev](https://sanghyunpark.pages.dev)) pins a release in its `webapps.json` and serves it at `/apps/groovix/`.

## License

The code is under the [MIT License](LICENSE). The recorded instrument sounds in `samples/` are not
covered by it: they keep their own Creative Commons Attribution 3.0 license, listed in [CREDITS.md](CREDITS.md).

---

## 한국어

브라우저에서 돌아가는 3트랙 그루브박스입니다. 신스와 실제 녹음 악기, 16칸 드럼 머신, 루프 녹음,
콧노래를 음표로 바꾸는 목소리 트랙, 그리고 하우스·로파이부터 보사노바·뽕짝·삼바, 파헬벨의 캐논까지 예시 믹스 26곡이 들어 있습니다.
화면은 한국어·영어·일본어를 지원합니다. 라이브러리 없이 HTML, CSS, 자바스크립트와 웹 오디오만으로 만들었습니다.
코드는 [MIT 라이선스](LICENSE)를 따릅니다. 녹음 악기 소리는 여기에 포함되지 않으며, 출처와 라이선스(CC BY 3.0)는 [CREDITS.md](CREDITS.md)에 있습니다.
