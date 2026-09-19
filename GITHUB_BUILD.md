# GitHub build instructions

1. Create a free GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Commit to the `main` branch.
4. Open **Actions**.
5. Select **Build RumiVet AI APK**.
6. Click **Run workflow**.
7. When it finishes, open the workflow run and download **RumiVet-AI-debug-apk** from Artifacts.
8. Extract the artifact and install `app-debug.apk` on Android.

## Notes
- The workflow uses JDK 17 and Gradle 8.9, compatible with the project's Android Gradle Plugin 8.7.3.
- GitHub's Ubuntu runner supplies the Android SDK needed for the build.
- The debug APK is suitable for testing and sideloading. It is not a Play Store release.
- For Google Play distribution, configure signing and build an AAB with a protected signing key.
- The repository includes `gradlew` and `gradlew.bat`. The workflow regenerates the wrapper at build time to ensure the wrapper JAR matches Gradle 8.9.
