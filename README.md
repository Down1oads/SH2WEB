# Silent Hill 2 Web

Experimental PS2 static recompilation for desktop browsers.

Play at https://down1oads.github.io/SH2WEB/ and select your local Silent Hill 2
USA v2.01 ISO (3,879,108,608 bytes). No Steam login, installation, or local server
is required. The ISO is read locally in chunks and is not uploaded. Select it
again after reloading the page. Use current Chrome, Edge, or Brave with WebGPU
and hardware acceleration. Click the game or press a key to enable audio.

The title, opening, bathroom, and observation deck have been tested, with roughly
60 displayed/runtime FPS in tested areas. Later progression, combat, and the
whole game remain unverified. This is a work in progress, not a completed port.
All 23 stage modules are compiled; that does not establish full playability.

The player keeps the original game logic and uses ps2-web-recomp, which statically
recompiles EE code to WebAssembly while modeling PS2 hardware and interpreting
the IOP. Upstream: https://github.com/snuri00/ps2-web-recomp at
76554ba44166791654b31407b1e466366418599b. Its MIT license is included in
LICENSE-runtime.txt. Silent Hill 2 belongs to its respective rights holders;
this is an unofficial project.

Controls: see [CONTROLS.md](CONTROLS.md). Memory cards use browser storage;
clearing site data removes them. During play only the game and green FPS
counter are shown. Initial setup selects the disc and then launches automatically.

## Hosting

These are prebuilt static files. In repository Settings → Pages, choose
Deploy from a branch, main, / (root). No build workflow is needed. The service
worker supplies cross-origin isolation headers for threaded WebAssembly on
GitHub Pages. A first visit may reload once. Serve over HTTPS or localhost;
opening index.html directly from disk will not work.
