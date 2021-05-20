# deferred_crash

Steps:
- `flutter build appbundle --release`
- `bundletool build-apks --local-testing --bundle build/app/outputs/bundle/release/app-release.aab --output test.apks`
- `bundletool install-apks --apks test.apks`
- Launch app
- Observe instant crash (you can use `pidcat com.example.deferred_crash` or logcat to view stack trace)
