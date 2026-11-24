# Build and CI — planning only

GitHub Actions is a candidate for automated Android APK builds after engine selection. No workflows, exports, credentials, signing keys, runner purchases or build execution have been configured.

Before activation:
1. Select engine and pin tool versions.
2. Verify GitHub Actions availability, runner and artifact quotas, and workflow write permissions.
3. Set up the appropriate Android export toolchain (SDK, JDK, engine templates).
4. Establish reproducible debug APK export and automated checks.
5. Use GitHub encrypted secrets for release signing only when needed. Never commit signing keys or tokens.
6. Test APK on real hardware; measure frame time, memory, load times and thermal behavior.

A cloud build is not a substitute for a 3D editor or device testing.