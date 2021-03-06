# Releasing a new version

1. Make sure you're on the `master` branch

1. Make sure that the library version in both `BlueprintUI.podspec` and `BlueprintUICommonControls.podspec` is correct (it should match the version number that you are about to release).

1. Create a commit and tag the commit with the version number
   ```bash
   git commit -am "Releasing 0.1.0."
   git tag 0.1.0
   ```

1. Push your changes
   ```bash
   git push origin master && git push origin 0.1.0
   ```

1. Publish to CocoaPods
   ```bash
   bundle exec pod trunk push BlueprintUI.podspec
   bundle exec pod trunk push BlueprintUICommonControls.podspec
   ```