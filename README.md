# Hood Ninjaz wikis

Two self-contained wikis published with GitHub Pages from the `gh-pages` branch, each behind a passphrase gate.

- `codex/` The Danim Codex, the canon wiki.
- `anime-guide/` The Anime Guide, the craft library.
- `index.html` A landing page linking to both.

Each wiki page is encrypted whole (AES-256-GCM, PBKDF2-SHA256 key derivation) and decrypted in the browser with the Web Crypto API. This repository only ever holds ciphertext; the passphrase is not in it. Built and pushed by `tools/publish-wikis.sh` in the private Vision repo, which regenerates the pages from markdown. Do not edit these files by hand: the next publish overwrites them.
