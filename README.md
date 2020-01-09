# Flash Chat

Flash Chat is from London App Brewery's Flutter course in LinkedIn Learning.
You will need to create your own Firebase credentials and put them in the appropriate folders for Android and iOS.

# Troubles during following the course
1. Encountered this error:
flutter com.android.builder.dexing.DexArchiveMergerException: Error while merging dex archives: The number of method references in a .dex file cannot exceed 64K.

   To solve this, I changed minSdkVersion to 21 in android/app/build.gradle as per [this link's]             (https://github.com/flutter/flutter/issues/20747#issuecomment-536337915) advice.

2. Chat messages not in order

   When a user sends a new message a new document will be created and will be added to the collection in Firestore, but the auto-generated document IDs are not ordered. Thus, during retrieval, the chat messages will not appear in order as well.

   To solve this, I added a createTime property and sort on retrieval.

This application was built using:
- Flutter v1.12.13+hotfix.5
- Dart 2.7.0
