# IETE Forum Desk

Coordination dashboard for the IETE Student Forum, SVCE: meeting agendas, team updates, events, decisions, follow-ups, attendance and responsibilities. Missing information is flagged instead of guessed.

Static site (no build step) with Firebase Firestore for shared data and Google sign-in.

## Setup
1. Create a Firebase project. Enable **Authentication > Google** and create a **Firestore** database.
2. Copy your web app config into `firebase-config.js`.
3. Put the allowed Google emails in `firestore.rules` and publish the rules (Firestore > Rules).
4. Add your site's domain (for example `your-name.github.io` or your Vercel domain) under Authentication > Settings > Authorized domains.
5. Deploy: GitHub Pages (Settings > Pages > main branch, root) or Vercel (import the repo, no build command).

## Data
Collections: `people`, `updates`, `events`, `decisions`, `followups`, `meetings`, `agenda`, and one document `meta/meeting`.
Do not commit member phone numbers or other personal data to this repo.
