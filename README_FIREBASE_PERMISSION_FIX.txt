SHAMBHU SHED - FIREBASE PERMISSION FIX

This package includes firestore.rules and firebase.json.
The rules cover all Firestore paths currently used by the app:
- shambhuSync
- shambhuMoistureStacks
- shambhuMoistureEntries
- shambhuAccessRequests
- shambhuAccess/* (including shambhuAccess/control)

IMPORTANT:
The app cannot change Firestore Security Rules by itself. Deploy the included
firestore.rules to the Firebase project used by the app (projectId:
shambhu-shed).

Firebase Console method:
1. Open Firestore Database -> Rules.
2. Replace the existing rules with the contents of firestore.rules.
3. Publish.

Firebase CLI method from this package folder:
  firebase deploy --only firestore:rules --project shambhu-shed

Anonymous Authentication must also be enabled because the app uses
signInAnonymously().
