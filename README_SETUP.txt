WELSEAT ADMIN PANEL — MOTION EDITION

Upload index.html and app.js to the ROOT of a NEW GitHub Pages repository.
Enable GitHub Pages: Settings > Pages > Deploy from branch > main > /(root).
Add welseat.github.io to Firebase Authentication > Settings > Authorized domains.
Enable Email/Password provider.

Admin login uses existing Firebase Auth email/password. Access is granted only if Firestore admins/{AUTH_UID} exists with role: "admin".
The admin can approve/suspend partners, view referral leads, set commission, update lead status, mark payout Paid/Unpaid, and export CSV.

This panel shares the same Firebase project and collections as the Welseat Partner Motion panel:
partners/{uid}, leads/{leadId}, admins/{uid}.
Publish the matching firestore.rules from the Partner package before use. Never make Firestore public.
Commission is manually confirmed by admin after checking a successful purchase. This does not automate WooCommerce verification or money transfer.
