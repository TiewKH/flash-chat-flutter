# Flash Chat

Flash Chat is from London App Brewery's Flutter course in LinkedIn Learning.
You will need to create your own Firebase credentials and put them in the appropriate folders for Android and iOS.

# Troubles during following the course
1. Encountered this error:
flutter com.android.builder.dexing.DexArchiveMergerException: Error while merging dex archives: The number of method references in a .dex file cannot exceed 64K.

To solve this, I changed minSdkVersion to 21 in android/app/build.gradle as per [this link's](https://github.com/flutter/flutter/issues/20747#issuecomment-536337915) advice.

2. Messages not in order
When documents are added to the collection in Firestore, the document ID are not ordered.

To solve this, I added a createTime property and sort on retrieval.

This application was built using:
- Flutter v1.12.13+hotfix.5
- Dart 2.7.0
