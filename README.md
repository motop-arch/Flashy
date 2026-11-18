# Flashcards (Android)
Offline Chinese flashcard app: HTML/JS UI (www/index.html), IndexedDB storage, wrapped with Capacitor.
## Get the APK (no Android Studio needed)
1. Create a GitHub repo, upload this folder, push.
2. Actions tab → "Build APK" → run → download artifact `flashcards-apk` → unzip → flashcards.apk (debug-signed, installable).
3. Copy the APK to your phone, open it, allow "install unknown apps".
Locally: `npm install && npx cap add android && npx cap sync android`, open `android/` in Android Studio → Build APK.
## Import
Home → Import file → pick CSV/TXT/JSON (+ optional image/audio files matched by name in `image`/`audio` columns) → preview → name deck → Confirm.
Columns (any order, header row): chinese, pinyin, english, additional, explanation, example, example_translation, image, audio, notes, grammar, category. Only chinese is required.
TXT: tab- or |-separated, header optional (then order is chinese|pinyin|english|…). JSON: list of cards or {"name":"…","cards":[…]}. JSON may also embed media as data: URLs.
## Backup
Settings → Back up everything (share/save the JSON). Restore: Settings → Restore, choose the file. Deck → Export saves one deck (restore it the same way).
