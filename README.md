# TVCalendar
Responsive family calendar with live Firebase sync, optimized for phones and widescreen TVs.

## Publish
GitHub Settings > Pages > Deploy from a branch > main > root. Allow a few minutes for deployment.
Phone: https://keubanks16.github.io/TVCalendar/
TV: https://keubanks16.github.io/TVCalendar/?tv=1

## Firebase setup
Enable Email/Password Authentication and Firestore in project tvcalendar-b2b59.
Publish the included firestore.rules in Firebase Console > Firestore > Rules.
Create a Firebase Auth user in Authentication > Users, copy their UID.
In Firestore, create collection households, document family, subcollection members, document <UID>, field role (string) = owner.
Sign in with the same email and password on phone and TV. Events will update automatically.
Only provision trusted accounts as members. Rules intentionally block self-enrollment.
If the screen shows a permissions error, check that the UID exactly matches the membership document.
No Google Calendar sync yet.